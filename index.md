---
layout: default
title: Home
---

{% assign list = site.pages | where_exp: "page", "page.path contains 'posts/'" %}

<div>
    {% for page in list %}
        <div class = "post">
            <div class = "header">
                <a href = "{{ page.url }}">{{ page.title }}</a>
                <div class = "date">{{ page.date }}</div>
            </div>
            <div class = "description">{{ page.description }}</div>
            <div class = "tags">
                {% for tag in page.tags %}
                    <span class = "tag">#{{ tag }}</span>
                {% endfor %}
            </div>
            <img src = "/images/{{ page.image }}">
        </div>
    {% endfor %}
</div>

<style>
    .post {
        padding: 20px;
        margin-bottom: 20px;
    }
    
    .post .header {
        display: flex;
        justify-content: space-between;
        gap: 20px;
    }
    
    .post .header .date { 
        text-align: right;
    }
    
    .post .description {
        margin-bottom: 20px;
    }
    
    .post .tags {
        margin-bottom: 20px;
    }
    
    .post .tags .tag {
        color: gray;
    }
    
    .post a {
        margin-bottom: 20px;
        display: inline-block
    }
    
    .post img {
        width: 100%;
        object-fit: cover;
        aspect-ratio: 16 / 9;
    }
</style>
