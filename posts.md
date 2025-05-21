---
layout: default
title: Blog Posts
---

<h1>Blog Posts</h1>
<ul>
  {% for post in site.posts %}
    <li>
      <a href="{{ post.url }}">{{ post.title }}</a> ({{ post.type }})
    </li>
  {% endfor %}
</ul>
