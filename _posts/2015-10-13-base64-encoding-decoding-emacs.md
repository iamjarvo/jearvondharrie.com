---
layout: post
title: Base64 encode and decode in Emacs
category: blog
tags: emacs, base64
year: 2015
month: 10
day: 13
published: true
summary: Base64 encoding and decoding in Emacs
---

### Problem

Need to Base64 encode or decode a region

### Solution

To encode, highlight the region and `M-x` `base64-encode-region` 

To decode, highlight the region and `M-x` `base64-decode-region`

More info in the <a href="http://www.gnu.org/software/emacs/manual/html_node/elisp/Base-64.html">docs</a>

<em>Thanks to <a href="https://twitter.com/jwinter">jwinter</a> for showing this to me.</em>
