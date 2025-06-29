---
layout: default
title: Home
---

# Welcome to Janith's

A technocrat's journey through code, ideas, and digital innovation.

## Latest Posts

{% if site.posts.size > 0 %}
<ul class="post-list">
  {% for post in site.posts limit:5 %}
    <li>
      <div class="post-meta">{{ post.date | date: "%B %d, %Y" }}</div>
      <h3 class="post-title">
        <a href="{{ post.url | relative_url }}">{{ post.title | escape }}</a>
      </h3>
      {% if post.excerpt %}
        <p>{{ post.excerpt | strip_html | truncatewords: 30 }}</p>
      {% endif %}
    </li>
  {% endfor %}
</ul>

<p><a href="/blog/">View all posts →</a></p>
{% else %}
<p>No posts yet. Check back soon for insights on code, technology, and digital innovation.</p>
{% endif %}

## Featured Apps

<div class="app-grid">
{% for app in site.apps limit:3 %}
    <div class="app-card">
        {% if app.icon %}
        <img src="{{ app.icon }}" alt="{{ app.title }} icon" class="app-icon">
        {% endif %}
        <h3 class="app-title">{{ app.title }}</h3>
        <p class="app-description">{{ app.description | truncatewords: 20 }}</p>
        <div class="app-links">
            <a href="{{ app.url }}" class="app-link">Learn More</a>
            {% if app.links %}
                {% for link in app.links %}
                    {% if link.primary %}
                    <a href="{{ link.url }}" class="app-link primary" 
                       {% if link.url contains 'http' %}target="_blank" rel="noopener"{% endif %}>
                        {{ link.text }}
                    </a>
                    {% endif %}
                {% endfor %}
            {% endif %}
        </div>
    </div>
{% endfor %}
</div>

{% if site.apps.size > 3 %}
<p><a href="/apps/">View all apps →</a></p>
{% endif %}