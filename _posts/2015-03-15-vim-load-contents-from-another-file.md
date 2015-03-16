---
layout: post
title: Load contents of another file into the current file in Vim
category: blog
tags: vim, tidbit, tooling, editor
year: 2015
month: 3
day: 15
published: true
summary: Vim trick
---

### Problem

Need the contents of another file in the current file.

### Solution

Vim's Ex command `read`.

```vim
  :read path/to/needed/file
```

<script type="text/javascript" src="https://asciinema.org/a/17735.js" id="asciicast-17735" async></script>
