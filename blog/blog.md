---
layout: page
title: Blog
permalink: /blog/
---

this is the blog page

<ul>
  {% for post in site.posts %}
    <li>
      <a href="{{ post.url }}">{{ post.title }}</a>
    </li>
  {% endfor %}
</ul>