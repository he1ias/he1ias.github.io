---
layout: default
title: Home
---

# Posts
<ul>
    {% assign list = site.pages | where_exp: "page", "page.path contains 'posts/'" %}
    {% for page in list %}
        <li><a href = "{{ page.url }}">{{ page.title }}</a></li>
    {% endfor %}
</ul>
