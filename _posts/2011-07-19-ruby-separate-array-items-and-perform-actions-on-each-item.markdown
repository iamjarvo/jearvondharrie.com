---
layout: post
title: "Ruby Separate Array Items and Perform Actions on Each Item"
date: 2011-07-19 04:23:55
comments: true
categories:
---

Ever wanted to separate the values in an array and also link them to
something. Before I knew about the map method I used each_with_index. I
knew this wasn't very railseque. Below is a snippet using the
each_with_index.

``` ruby
    #authors is an array and loop through with each_with_index. Returns
    author then index.
    #on each iteration make an a tag using link_to and link it to the
    author. Add a comma to the end unless its the last one in the index(-1
    signifies the last key in the array)
    @authors.each_with_index do |author, index| 
      link_to author.name, author_path(author) 
       ', ' if index < @authors.count - 1
    end
```

This can be more railseque by using the map method.

Map is defined in apidock as 'Returns a new array with the results of
running block once for every element in enum.' What this basically means
is it will loop over the array and make changes to the each item in the
array and then add it to a new temporary array.

``` ruby
    @authors.map do |author|
      (link_to author.name, author_path(author)).join(,).html_safe
    end
```

``` ruby
    @authors.map do |author|
```
Above line is the map method 

``` ruby
    (link_to author.name, author_path(author)).join(,).html_safe
```
Above line is the block of code that runs on each array item. When the
map method is done it returns an array with however many elements and
then we concatenate those with a join. I found that the join was printing
out the html tags as a string so I used .html_safe to have it print out
html code also. This way handles the last comma issue without
the extra code. Very railseque I would say!

