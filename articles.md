---
layout: default
title: Articles
permalink: articles.html
---

<h2 class="post_title">Featured</h2>
<ul class="posts">
  {% for post in site.categories.featured %}
    <li><span>{{ post.date | date_to_string }}</span> &raquo; <a href="{{ post.url }}">{{ post.title }}</a>
    <p>{{ post.excerpt }}</p>
    </li>
  {% endfor %}
</ul>

<h2 class="post_title">Articles</h2>
<ul class="posts">
  {% for post in site.categories.articles %}
    <li><span>{{ post.date | date_to_string }}</span> &raquo; <a href="{{ post.url }}">{{ post.title }}</a></li>
  {% endfor %}
</ul>
