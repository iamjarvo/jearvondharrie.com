---
layout: post
title: "Bookmarklet for Opening Links in a New Tab"
date: 2011-08-25 23:52
comments: true
categories: 
---

I have come across multiple people complianing about site like hackernews or google not opening links in a new tab. So I made a simple bookmarklet that gives the user the preference to open links in a new page with a click.

<a href="javascript:(function (){if(document.getElementsByTagName('a')){anchors = document.getElementsByTagName('a');for(var i = 0;  i < anchors.length; i++){anchors[i].setAttribute('target', 'blank') ;}}}());">NT</a>

Basically just drag the "NT" to the bookmark bar and then click it when you are on the page. When you get to hacker news or are finished with your google search, click the bookmark in your bookmark bar. Links will then be opened in a new tab.
