---
layout: post
title: "Using Shortcodes in Wordpress Widget Areas"
date: 2011-05-30 14:47:57
comments: true
categories: 
---

Have you ever wondered how to use shortcodes in wordpress widget areas?  All it takes is a simple filter.

``` php
    add_filter('widget_text', 'do_shortcode');
```
