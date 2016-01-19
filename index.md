---
layout: default
title: Home
---

Tackling engineering design problems using tools from convex optimization and computer science.

### Recent posts
<div class="posts">
  {% for post in site.posts %}
    <span>
      <a href="{{ post.url }}">{{ post.title }}</a>
      |
      {% if post.author %}{{ site.data.authors[post.author].name }},{% endif %}
      {{ post.date | date_to_string }} 
    </span>
  {% endfor %}
</div>
