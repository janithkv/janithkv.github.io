---
layout: default
title: Apps
permalink: /apps/
---

# Apps

A collection of applications and tools I've built to solve everyday problems with clean, efficient code.

<div class="app-grid">
{% for app in site.apps %}
    <div class="app-card">
        {% if app.icon %}
        <img src="{{ app.icon }}" alt="{{ app.title }} icon" class="app-icon">
        {% endif %}
        <h3 class="app-title">{{ app.title }}</h3>
        <p class="app-description">{{ app.description }}</p>
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