---
layout: post
title: "ERROR 2002 (HY000) - Rails MySQL"
date: 2011-11-20 15:53
comments: true
categories: 
---

Rails uses sqlite3 by default, but I wanted to use mysql. Reason for this is I had set up MySQL on my vps already and wanted to use the same db technology for dev and producton. Coming from a php background my computer was already using MAMP pro for php and MySQL, so I decided to just use MAMP pro. Even though I had the right credentials in the database.yml file I kepy getting the ERROR 2002. I tried switching the host to 127.0.0.1 but it did not work. The solution that I came up with is to delete the host line and add a socket line.

```
  socket : /path/to/socket
```
