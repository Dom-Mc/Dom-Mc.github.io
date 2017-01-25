---
layout: post
title:  "Rails Meets Ajax"
date:   2016-12-05 18:59:18 +0000
---


For our jQuery/Rails assessment at learn.co, we were tasked with taking our newly acquired knowledge from the latest section (JS/jQuery/JSON/API/Ajax) and applying it to the rails project we had completed in the previous section.  The objective was to add functionality which would enable the frontend of the application to communicate with the backend via ajax.

Do to the restful architecture of Rails’ routing along with convenient serializing gems such as Active Model Serializer, it doesn’t take a whole lot of configuration to turn a stereotypical rails application into a fully functional api.  Even before additional advancements offered in Rails 5, connivence methods such as respond_to and render make it surprisingly simple to enable your routes (endpoints) to not only respond in html, but also to handle requests in both json or even javascript.

Now to gain a little more experience in the process of both sending and receiving ajax requests, we weren’t able to use the remote: true option offered by Rails which automatically (and somewhat magically) converts a form submission into ajax.  Therefore we had to build out the ajax request by hand (aka the old fashion way), however that’s not even an accurate portrayal thanks largely to jQuery.

While the requirements by themselves weren’t complicated to implement, it was indeed challenging to a finished project and changing/bending it in somewhat unnatural directions.  At the same time it provided an opportunity to learn the art of adaption because these are challenges we’ll face as developers going forward.  The life of an application isn’t linear and it will be essential to adapt to constant changes and demands of a project.  Learning how to build modular applications with the ability to scale is a large part of web development architecture and this project was perhaps our introduction.

-by Dominic McKellar

[Project Keeper](https://dom-mckellar-fetchit.herokuapp.com/) - [Github](https://github.com/Dom-Mc/fetch_it)
