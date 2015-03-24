---
layout: post
title: "Capistrano Deployment Woes: Old Files/templates Being Used"
date: 2011-10-04 10:53
comments: true
categories: 
---

I have published my first app with rails. It can be viewed <a href="clarencedauphinotinvitational.com">here</a>. To deploy my app on my server I decided to use github and capistrano. 
Even though I deployed a new copy I noticed that actionmailer was using old files with old configs. I thought it was a caching issue but it was not. I was using resque to queue up my emails.
So I was starting the queue for resque manually. I tried stopping and restarting the queue but it did not help. Since capistrano symlinks the current folder with the latest release folder, when 
I cd to the current folder it went to the latest release folder. When I pushed a new release there would be a new release folder but my queue would still be running in the old release folder. 

<h3>Solution</h3>
 This is partly my fault because things should be automated. I should have wrote a task that automated restarting the queue. At the time I didn't know a lot about capistrano and I was under a deadline. To fix this everytime you deploy, stop the queue, cd out the current folder, cd back into the current folder and start the queue.
 So if you are using anytime of process that relies on running from a folder this solution should work.
