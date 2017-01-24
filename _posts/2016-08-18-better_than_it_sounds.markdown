---
layout: post
title:  "Better Than It Sounds"
date:   2016-08-18 18:50:05 -0400
---


Having just completed the Sinatra section at [learn.co](https://learn.co), now is as good of an opportunity as any to share some thoughts on both [my project](https://github.com/Dom-Mc/project_keeper) and the ruby framework. I’ll be honest, at the beginning I wasn’t too excited about devoting an entire section to Sinatra. I didn’t quite understand the need to learn another web application framework right before Rails. Well, I was wrong.

I immensely enjoyed the lightweight framework and found it extremely helpful in reenforcing certain concepts I had somewhat struggled with in the past. Leading up to Sinatra I had a general understanding of terms such as *CRUD*, *MVC*, and *Rest*. However I now appreciate the flexibility Sinatra has to offer, as it gave me an opportunity to experiment and actually implement those concepts into practice.

As for my Sinatra project itself, we were required to create an application to track something of personal importance. Deciding on a domain was pretty simple for someone juggling what seems to be an endless amount of projects. Hmmmmm…. I have a ton of projects and I could really use a way to stay on top of them, `<sarcasm>if only I had an idea for a Sinatra application.</sarcasm>`

I came up with a mini blueprint for constructing the app. I’m a "visual learner" and I found jotting down a rough outline to be pretty helpful in the early stages. Coming up with models and their corresponding relationships was straight forward. The project only needed two models, a User and a Project. Again a simple *has many* - *belongs to* relationship. A User could have many Projects and each Project would belong to a single User. I did however go back and forth between what attributes to include in the database and what column restraints to apply. In retrospect I was probably a bit too specific, as I found myself removing some requirements in an attempt to provide the user with greater flexibility. I found it useful to look at the application from the users’ perspective and in doing so I ended up choosing a more flexible/user friendly approach. For example at first a lot of my table columns were required, such as "date_started" and "deadline". However the more I thought about it, I came to realize there may be edge cases where perhaps a user didn’t have a deadline. What about a situation where a user couldn’t remember a start date or simply didn’t care to add one. Did I want to create an application where a user would be required to make up imaginary dates in order to take advantage of the application? Of course not so I began to make some adjustments. Overall that may just be my biggest take away from the project. True I’m the one developing the application, but what good is creating an incredible app without any users? Well let’s be honest, calling it "incredible" would be highly subjective under those circumstances.

Finally, much like this blog post, one of the most challenging aspects was deciding on a stopping point. Regardless the level of resistance, I always managed to find one final feature to tweak, another media query to add, or one last scan for potential code begging to get refactored. I had to constantly remind myself that a programming bootcamp is somewhat like a marathon, *NOT* a sprint. And no matter what, I must… keep… moving.

- by Dominic McKellar
[Project Keeper](https://dom-mckellar-projectkeeper.herokuapp.com/) - [Github](https://github.com/Dom-Mc/project_keeper)
