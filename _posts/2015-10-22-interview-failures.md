---
layout: post-light-feature
title: "Coding Test Failures"
category: rails
tags: []
---
> Right after I fail a coding test, the solution is right in front of me.

### The Problem (similar to codibility but differs in difficulty)
Algorithm problem taken down due to DMCA violation. Was hoping this would help people but sorry, I can't post the problem anymore.

### My Solution
```
test_cases = [
  [[1,3,1,4,2,5],7,3], #3
  [[1,3,1,4,2,5],8,3], #5
  [[1,3,5,7,10,5],9,3], #3
  [[1,3,1,4,2,5],8,2], #-1
  [[1,3,5,10,7,5],11,2], #-1
  [[1,3,5,10,7,9],12,2], #5
  [[12,10,8,6,4,2],12,2] #5
]

# Expected Time O(N) Space O(X)
def frog_jump(a,x,d)
  if x <= d
    return 0
  end
  mid_low = nil
  mid_high = nil
  last_position = 0

  a.each_with_index do |position, time|
    if position > last_position && (position - last_position) <= d
      last_position = position
    elsif x > position && (x - position) <= d
      x = position
    elsif position > last_position && position < x
      if !mid_low && !mid_high
        mid_low = position
        mid_high = position
      else
        if position > mid_high && (position - mid_high) <= d
          mid_high = position
        elsif position < mid_low && (mid_low - position) <= d
          mid_low = position
        end
      end
    end
    puts "start: #{last_position} mid: #{mid_low} #{mid_high} dest: #{x}"

    # check for solution
    if !mid_low || !mid_high
      if (x - last_position) <= d
        return time
      end
    elsif (mid_low - last_position) <= d && (x - mid_high) <= d
      return time
    end
  end
  return -1
end

```
Obviously, this is not the best solution but it is something that fulfills the constraints I believe. (Just ugly code with bunch of if and else's though)

Initially, I provided a solution that updated the last_position but it only worked when the array was in order of values. Then, I kept considering solutions that would solve the out-of-order problem but kept getting stuck because they wouldn't meet the time complexity constraint. A day later after failing the question, I thought of going through it in my head while eating my dinner and solved it within 2 minutes. easy...I actually came up with the idea of mid_low and mid_high during the interview but my impulsive thoughts told me they ran into issues as I thought through them. Sigh...back to grinding through applications again.
