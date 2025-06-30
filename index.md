---
layout: default
---

## Recent Posts

{% for post in site.posts limit:5 %}
- [{{ post.title }}]({{ post.url }}) - {{ post.date | date: "%B %d, %Y" }}
{% endfor %}

## Apps

Check out my [Apps section](/apps/) to see what I'm currently working on.