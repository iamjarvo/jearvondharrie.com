---
layout: post
title: "Seven Languages in Seven Days - Ruby Day 1 Homework"
date: 2011-05-20 13:48:28
comments: true
categories: 
---

<p>I recently started reading the book <a href="http://www.amazon.com/Seven-Languages-Weeks-Programming-Programmers/dp/193435659X">Seven Languages in Seven Days</a>. I thought it would be a good idea to post the homework assignments. Below are the answers to the homework from ruby day one.</p>

``` ruby
    #ruby api
    www.ruby-doc.org/core/

    #free online version of pragmatic guide 
    http://www.ruby-doc.org/docs/ProgrammingRuby/

    #method that substitutes part of a string 
    phrase = 'Hello World'
    puts phrase.gsub('World', 'iamjarvo')

    #info about ruby's regular expression 
    http://www.regular-expressions.info/ruby.html

    #print the string "Hello World"
    puts 'Hello World'

    #find the index of the word Ruby in the string Hello Ruby 
    phrase = 'Hello Ruby'
    puts phrase.index('Ruby') #method is case sensitive 

    #print name 10 times
    i = 0
    while i < 10
     puts 'iamjarvo'
     i = i + 1
    end

    #print the string this is is sentence number 1, the number 1 changes from 1 to 10 
    for i in (1..10)
     puts "this is sentence number #{i}"
    end

    #running a ruby program from file
    when in the directory type ruby filename 

    #bonus
    #pick a random number then have the user guess. tell them if they are hot or not 

    rand_num = rand(10)
    puts rand_num
    puts "Please input your guess"
    #guess = gets.chomp

    while true 
      guess = gets.chomp.to_i
      #guess > rand_num ? puts 'Too high try again ' : puts 'too low try again'
      #puts "Your answer is #{guess < rand_num ? 'low' : 'high'}"
      if guess == rand_num
        puts 'You are right'
        break
      elsif guess < rand_num
        puts 'too low'
      else
        puts 'too high'
      end
    end
```
<p>Disclaimer: Some of the answers might not be rubyesque but I am using what the book taught so far.</p>
<p>Thanks to <a href="http://twitter.com/#!/matschaffer">@matschaffer</a> for double checking the answers!</p>
