---
layout: post
title:  "Modern Web Site Development Mess"
date:   2021-06-02 10:57:00 -0000
categories: web development
---

### TL;DR

I have been out of web site development for a while, and now, when I need to build a simple website for my side project, i discovered a lot of new frameworks and completely lost.

I understand that develops constantly stive to create new tools to make front and back end more scalable and easy to develop. Ultimatly, the less time we need to spend to build and maintain the code the better. However, it feels that the learning curve is unnessesary too steep.

And it is not that packages do not make sense. Surely, all of them bring some value. but it looks like a 'Whild West'. There are so many different packages that seemingly doing the same thing. There are so many different ways of doing the same thing and it becomes not so obvious why someone should choos one set of packages over another. 

Here I am describing my path through the maze of web packages.

### Project Overview

To set the stage, my project is not that complicated though requires use of multiple different technologies.

Here are the requirements:
1. User Authentication and authorization.
2. Obviousely that would require Registration and Profile pages.
3. I needed to allow users to upload thier data to the site in predefined CSV format.
4. Once file is uploaded that should trigger file processing job that saves data in the format consumable by the web pages.
5. Data will be displayied in tables.
6. User can sort, filter, search, add tags and save the preferences.
7. Some of the data will need to be precalculated to be diplayed in charts.

From the get go I decided to not spend time reavieing Python of Ruby frameworks. In addition, I feel that Java and .Net are a bit obsolete and discarted them too.

There seems to be a lot of gravitational force to use Node.js or related Java Script packages. I was curious about React for a while and thought that it would be a good opportunity to learn the frameowrk.

To store data on the backend I had several options:
1. AWS - seems to be the leader in cloud technologies. A lot of companies are choosing them by default, but it would take me a bit more time to set everything up there.
2. Firebase - is very similar to AWS in capabilities and it seems a bit more intuitive to setup.
3. Asure - is trying to compete with AWS, but Microsoft left a bitter taste in my mouse. So I decided not to spend much time with them for now.
3. Other cloud providers like Heroku, and Cloudflare could be a good alternatives. I kept them on the back burner of my research.

Thus, I decided to start with Firebase. I figured I can switch to AWS if things not going to work out or when I will have more clear picture of what my architecture going to look like.

My breif look at Firebase showed that it has most of the components I need off the shelf:
1. Firebase Auth - allows to setup user Authentication and Autharization. I hae built a small prototype proving that it works as expected and relativly easy to setup.
2. Firebase Store - this is equivalent of the AWS S3 buckets for various file types. I decided to use it to store user uploaded files. 
3. Firebase Storage (or Cloud, they seem to change the name) - is Document based database that I can use to store data for the web site.
4. Firebase Function - this is similar to AWS Lambda and should allow me to put backend code there. This is the only component that Google requires an upgrade to a paid account.

I was able to built simple prototype for all the components with a free account, but the Function. I figured the amount of traffic my site is going to generate initially should not trigger any payments. I assumed that Firebase Function should allow me to build RESTfull APIs, but it is the only peice I haven't prototypes.


After building all the small pieces in isolation. I was ready to build site and put all this things together.

### React vs. Node vs. HTML vs. Express vs. Antything Else?










