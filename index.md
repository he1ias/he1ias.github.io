---
layout: default
title: Home
---

# Posts
<ul>
  {% assign pages_list = site.pages | where_exp: "p", "p.path contains 'posts/'" %}
  {% for p in pages_list %}
    <li><a href="{{ p.url }}">{{ p.title }}</a></li>
  {% endfor %}
</ul>
