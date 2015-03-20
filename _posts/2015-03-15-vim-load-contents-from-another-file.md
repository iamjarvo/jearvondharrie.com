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

<em>EDIT: I dislike having to delete the empty line. `:0r` will replace the current
line under the cursor.</em>

<script type="text/javascript" src="https://asciinema.org/a/17735.js" id="asciicast-17735" async></script>
