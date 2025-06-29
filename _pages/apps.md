---
layout: default
title: Apps
permalink: /apps/
---

<div class="posts">
  <h1>Apps</h1>
  <p>A collection of applications and tools I've built to solve everyday problems with clean, efficient code.</p>
  
  {% for app in site.apps %}
    <article class="post" style="padding-bottom: 2em; border-bottom: 1px dotted #ddd; margin-bottom: 2em;">
      
      <h2><a href="{{ site.baseurl }}{{ app.url }}">{{ app.title }}</a></h2>
      
      <div class="entry" style="display: flex; align-items: flex-start; gap: 1em;">
        {% if app.icon %}
        <img src="{{ site.baseurl }}{{ app.icon }}" alt="{{ app.title }} icon" style="width: 64px; height: 64px; border-radius: 8px; flex-shrink: 0;">
        {% endif %}
        
        <div>
          <p>{{ app.description }}</p>
          
          {% if app.tech_stack %}
          <div style="margin-top: 1em;">
            {% for tech in app.tech_stack %}
            <span style="background: #f4f4f4; padding: 2px 8px; border-radius: 12px; font-size: 0.8em; margin-right: 0.5em;">{{ tech }}</span>
            {% endfor %}
          </div>
          {% endif %}
          
          {% if app.links %}
          <div style="margin-top: 1em;">
            {% for link in app.links %}
            <a href="{{ link.url }}" style="margin-right: 1em; {% if link.primary %}font-weight: bold;{% endif %}" 
               {% if link.url contains 'http' %}target="_blank" rel="noopener"{% endif %}>
              {{ link.text }} →
            </a>
            {% endfor %}
          </div>
          {% endif %}
        </div>
      </div>
      
    </article>
  {% endfor %}
</div>