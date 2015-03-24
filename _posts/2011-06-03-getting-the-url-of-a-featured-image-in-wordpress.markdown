---
layout: post
title: "Getting the URL of a Featured Image in Wordpress"
date: 2011-06-03 06:32:39
comments: true
categories: 
---

Recently I was displaying the featured image of posts in a gallery format and wanted to show the larger version of the image in a shadow box. I needed to get the url of the large size image. I decided to get this using a few functions of wordpress. Below is the snippet with notes.

``` php
    // this snippet would be in a loop 
    //as the loop runs through the get_post_thumbnail_id() function will get the id of the image to the corresponding post 
    //we will need the id later
    $post_thumb_id = get_post_thumbnail_id();
    //we then use wp_get_attachment_image_src  to get attributes about the attachment
    //we pass in the id and the version of the image we want (I passed in original for the image size and it seemed to return the original image)
    //this function returns 3 items in an array [0] => url , [1] => width, [2] => height
    //we want url
    $attachment_info = wp_get_attachment_image_src($post_thumb_id, 'large');
    $attachment_src = $attachment_info[0];
    //we can then echo this variable anywhere
```
