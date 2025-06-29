---
layout: default
title: Blog
permalink: /blog/
---

# Blog

{% if site.posts.size > 0 %}
<ul class="post-list">
  {% for post in site.posts %}
    <li>
      <div class="post-meta">{{ post.date | date: "%B %d, %Y" }}</div>
      <h2 class="post-title">
        <a href="{{ post.url | relative_url }}">{{ post.title | escape }}</a>
      </h2>
      {% if post.excerpt %}
        <p>{{ post.excerpt | strip_html | truncatewords: 50 }}</p>
      {% endif %}
      {% if post.tags and post.tags.size > 0 %}
      <div class="post-tags">
        {% for tag in post.tags %}
        <span class="tag">{{ tag }}</span>
        {% endfor %}
      </div>
      {% endif %}
    </li>
  {% endfor %}
</ul>
{% else %}
<div class="empty-state">
  <p>No posts yet. Check back soon for insights on code, technology, and digital innovation.</p>
</div>
{% endif %}