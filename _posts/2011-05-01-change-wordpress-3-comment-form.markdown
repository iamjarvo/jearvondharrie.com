---
layout: post
title: "Change Wordpress 3 Comment Form"
date: 2011-05-01 22:06:49
comments: true
categories: 
---

<p>Wordpress 3 comes with a default comment form. The structure of this form might not be what you. To change this wordpress provides a function called <a href="http://codex.wordpress.org/Function_Reference/comment_form">comment_form</a>. </p>
<p>Comment form takes numerious arguments, but I will only show you two of them. Fields which handles the 3 defaults fields(name, email, and website) and comment_field which handles the text_area field. </p>
<p>First the arguments for the default fields must be specified. You can copy and paste the html from the old form and just make the changes you want. Keeping the name of the input fields is important but I would suggest keeping the ids the same</p>
``` php
    <?php
    $field_args = array(
        'author' => 
        '<p class="comment-form-author"><label for="author">Name (Required)</label>
        <input class="comment_form_custom" type="text" name="author" id="author" />
        </p>',
        '<p class="comment-form-email"><label for="email">Email (Required)</label>
          <input class="comment_form_custom" type="text" name="email" id="email" />
        </p>',
        'url' =>
        '<p class="comment-form-url"><label for="url">Website</label>
        <input class="comment_form_custom" type="text" name="url" id="url" /></p>',
        '<p><textarea></textarea></p>'
        );
    ?>
```	
<p>Then we can specify the arguments for the comment form. One of the arguments for comment form will take the field_args, the other will take the argument for the comment textarea. For the fields argument, a filter to the comment_default fields must be applied using the field_args.</p>
``` php
    <?php
    $new_comment_form = array(
      'fields' => apply_filters('comment_default_fields', $field_args),
      'comment_field' => '<p class="comment-form-comment"><label for="comment">Comment (Required)</label><textarea id="comment" name="comment" cols="45" rows="8"></textarea></p>'
    );
    );
    ?>
```
<h3>Summary</h3>
<p>To change the comment form you must specify the default field arguments then pass them into comment_form arguments along with the comment_field argument. It's important to keep the names of the inputs/textarea the same as the default structure. </p>
<h3>Where could you use this?</h3>
<p>You can use this to change the wording of the labels or the element that the inputs are in.This came in handy for me because I did not like the default structure of the comment form. For example asterisks were being used to show required fields, I wanted to word required to be displayed instead.</p>
