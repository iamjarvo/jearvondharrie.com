---
layout: post
title: "Managing Multiple Heroku Repos for the Same App"
date: 2012-02-17 18:15
comments: false
categories: heroku 
---

Recently I had to manage an app that had the staging and production version on
heroku. When pushing you don't have to worry about which version to push to
because each repo has a remote name, (i.e. heroku-staging, heroku-production).
When it comes to running app specific things though such as console you have to
pass in the app name with this flag --app appname. 

```
  heroku run script/console --app heroku staging
```
