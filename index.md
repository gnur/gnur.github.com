---
layout: page
title: blog.erwin.io
tagline: Writing about the world
---
{% include JB/setup %}

## What does it mean to write about the world?

I don't know, but it happens here.

## All Posts

<ul class="posts">
  {% for post in site.posts %}
    <li><span>{{ post.date | date_to_string }}</span> &raquo; <a href="{{ BASE_PATH }}{{ post.url }}">{{ post.title }}</a></li>
  {% endfor %}
</ul>


