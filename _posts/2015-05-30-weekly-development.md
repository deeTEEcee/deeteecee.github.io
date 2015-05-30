---
layout: post-light-feature
title: "Weekly Development"
description: ""
category: rails
tags: []
---

Since I recently got a new job, I've decided to development some kind of new feature that involves something that I'm rather unfamiliar with in order to push myself more. I used to always tell myself these things but i realized during the job search process how hard it is to push yourself, especially when you're so young like I am in my career. I guess what I'm saying is I want to increase my skillset in order to widen the range of apps I can create and the things I can do. However, it's a difficult

###Weekly Dev List

*Warning: this may not be readable. I will fix that when I get a bigger list.*

5/30: implement real-time notification on my stack overflow clone so that users can find that their questions were just answered. (to learn about websockets and perhaps a nice-looking notification library)

- What's the deal with web sockets and how it works with threads, processes, etc. (what's the default if im not using redis? is faye being used? what is faye?)
- Had to figure out what's a good way to separate the response from the current user from other clients. Best way I could think of is to just to save the user id somewhere (might be dangerous though so use a token instead) and handle the response and make sure the generated model is not the current user's if we would like to send that notification.

...*to be continued*
