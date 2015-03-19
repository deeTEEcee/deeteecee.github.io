---
layout: post-light-feature
title: "Ruby: {} block (single) vs do-end block (multi-line)"
description:
category: ruby
tags: [sample post, readability, test]
---
I had the following code to get the count of numbers in the array can divide y. Obviously, we have a problem and need to check if x==0 and for personal reasons, I wanted to do a multi-line block but it never runs!

```
[1,2,0,4].count {|x| y%x=0} 
[1,2,0,4].count do |x| 
	STDERR.puts 'IN FACT NO INPUT HERE AT ALL'
	next if x%=0
	y%x=0
end 

```
So what's going on? **The precedence** of {} over do-end. Even upon reading the stack overflow page I couldn't quite grasp it. Basically with {|x|}, the block is applied to count method but with do-end, it actually gets applied to [1,2,0,4] but well, you can't just pass a block to the array, it does nothing! Lesson done. 

Things learned for me other than the precedence:
- blocks don't return. Only whatever method is being used. Be very careful if you see "return" in blocks amidst nested methods.

For reference: 
http://stackoverflow.com/questions/5587264/do-end-vs-curly-braces-for-blocks-in-ruby