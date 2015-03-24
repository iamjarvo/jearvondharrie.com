---
layout: post
title: "Link_to Takes a Block!"
date: 2011-07-21 17:44:29
comments: true
categories: 
---

Have you ever wanted to surround a block of HTML with an a tag, for example a group of images. It is possible to do this because <a href="http://apidock.com/rails/ActionView/Helpers/UrlHelper/link_to" title="link_to" target="_blank"></a> takes a block. According to apidock the syntax is:

``` ruby
    link_to(url, html_options = {}) do
      # name
    end
```

In my idea situation i need to get the images for all the books in a certain genre and have them surrounded by one a tag. Reason I need this is because they are forming a slideshow. My code came out to be:

``` ruby
     <% link_to(genre_path(genre)) do %>
        <div class="home_gallery_images">
          <% books = books.shuffle %>
          <% for book in books %>
            <%= image_tag(book.cover.url(:medium)) %>
          <% end %>
      <% end %>
```
