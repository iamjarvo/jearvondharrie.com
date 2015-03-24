---
layout: post
title: "Rails/Haml Print HTML Element if Value Exists"
date: 2011-08-13 22:15:00
comments: true
categories: 
---

I am using a breadcrumb gem which is very handy. Its called <a href="https://github.com/weppos/breadcrumbs_on_rails" title="breadcrumb on rails" target="_blank">breadcrumb on rails</a>, I highly recommend you check it out. I had the gem rendering in my application layout file, and even though I didnt have a breadcrumb for certain controller it would still print the html element. My solution was to use a <a href="http://apidock.com/rails/ActionView/Helpers/TagHelper/content_tag" title="content_tag" target="_blank">content_tag</a> and an if statement. Below is the snippet.

``` ruby
    # bascially checks if @breadcrumbs has a value and if it does renders the html element and breadcrumb info
    = content_tag(:div, render_breadcrumbs, :class => 'breadcrumbs') if @breadcrumbs
```
