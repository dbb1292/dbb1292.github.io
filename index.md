---
layout: default
title: Home - God and You
---

<h2 class="post_title">Featured</h2>

<ul class="posts">
    {% for post in site.posts %}
      {% if post.category == "featured" %}
        <li><span class="date">{{ post.date }}</span><a href="{{ post.url }}">{{ post.title }}</a>
	<p>{{ post.excerpt }}</p></li>
      {% endif %}
    {% endfor %}
</ul>

<h2 class="post_title">Articles</h2>

<ul class="posts">
  {% for post in site.categories.articles %}
    <li><span class="date">{{ post.date }}</span><a href="{{ post.url }}">{{ post.title }}</a></li>
  {% endfor %}
</ul>
