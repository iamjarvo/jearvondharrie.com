---
layout: post
title: Create a hash from an array in Ruby
category: blog
tags: Ruby, hash
year: 2015
month: 5
day: 5
published: true
summary: Create a hash from an array in Ruby
---

### Problem

You would like to create a hash from an array or a nested array.

### Solution

Enter the [class method](http://ruby-doc.org/core-2.2.0/Hash.html#method-c-5B-5D) ```[]``` on Hash

```ruby
  # array
  array = [:uno, 1, :dos, 2, :tres, 3]
  Hash[*array] # => {:uno => 1, :dos => 2, :tres => 3}

  # nested array
  nested_array = [[:uno, 1], [:dos, 2], [:tres 3]]
  Hash[nested_array] = {:uno => 1, :dos => 2, :tres => 3}
```

Things to note with the array version:

* The array needs to contain an even number of elements
* The ```*``` operator needs to be used. It converts the array into method arguments.

<script type="text/javascript" src="https://asciinema.org/a/19541.js" id="asciicast-19541" async></script>
