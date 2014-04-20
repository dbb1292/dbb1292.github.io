---
layout: default
title: Home - God and You
---

<h2 class="post_title">Featured</h2>

<ul class="posts">
    {% for post in site.posts %}
      {% if post.category == "featured" %}
        <li>
	<ul class="tags">
	  {% for tag in post.tags %}
	    <li>{{ tag }}</li>
	  {% endfor %}
	</ul>
	<span class="date">{{ post.date | date: "%Y" }}</span>
	<a class="link_title" href="{{ post.url }}">{{ post.title }}</a>
	<div>
          {{ post.excerpt }}
	  <a class="moreLink" href="{{ post.url }}">read more</a>
	</div>
	</li>
      {% endif %}
    {% endfor %}
</ul>

<h2 class="post_title">Articles</h2>

<ul class="posts">
  {% for post in site.categories.articles %}
    <li>
      <ul class="tags">
        {% for tag in post.tags %}
	  <li>{{ tag }}</li>
        {% endfor %}
      </ul>
      <span class="date">{{ post.date | date: "%Y" }}</span>
      <a class="link_title" href="{{ post.url }}">{{ post.title }}</a>
    </li>
  {% endfor %}
</ul>
