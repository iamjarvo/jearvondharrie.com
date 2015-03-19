---
layout: post
title: Skip to next modified file in git
category: blog
tags: git, tidbit, tooling
year: 2015
month: 3
day: 18
published: true
summary: Jumping around in a git diff
---

### Problem

You would like to skip a large file in a [git diff](http://git-scm.com/docs/git-diff)

### Solution

Git sends the output of a diff to [less](http://unixhelp.ed.ac.uk/CGI/man-cgi?less). This
means you can use the less search navigation.
Each file in the diff starts with `diff`.

```sh
  /^diff
```

The above searches for the next line that starts with the word diff.

<script type="text/javascript" src="https://asciinema.org/a/17829.js" id="asciicast-17829" async></script>
