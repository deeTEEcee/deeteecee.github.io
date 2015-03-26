---
layout: post-light-feature
title: "Stack Overflow Clone Project"
description: ""
category: rails
tags: []
---
**Reason**: I had to write this quick mock-up using Rails and MongoDB. Honestly, I thought it wouldn't mean much on the MongoDB side but I learned a lot. Sure, I could have just plain googled the API for use in rails but I actually looked up what the difference was between NoSQL and RMDBS. Along with that, you have to be really careful when using "mongoid"-compatible gems because so many gems touch on the Active::Record set for RMDBS but a lot of them lack the support.

**Design**: Aside from that, I spent a lot more time on design along with functionality because I wanted this to be light and viewable for the interviewer. It's not the perfect design at the moment since I was trying to match stack overflow almost exactly but it looks nice enough to go through.

**Functionality**: I didn't hit too many hurdles. I was only requested to use MongoDB and put the basics of stack overflow: question-answer structure, a basic user, and markdown support. Luckily, we have the gems to do most of that. Now, I hope I added a little more than the interviewer was looking for (in terms of also adding rspec and a few other goodies)


For reference:
[stack overflow clone](http://stackoverflow-overflow-clone.herokuapp.com)
