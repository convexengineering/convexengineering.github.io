---
layout: default
title: Home
---

Tackling engineering design problems with tools from convex optimization.


### Recent posts
<div class="posts">
  {% for post in site.posts %}
    <span>
      <a href="{{ post.url }}">{{ post.title }}</a>
      |
      {% if post.author %}{{ site.data.authors[post.author].name }},{% endif %}
      {{ post.date | date_to_string }}
      <br>
    </span>
  {% endfor %}
</div>


### News
<div class="news">
<p>
  2016-03-29:
  Congratulations to Mike Burton on winning an NSF Graduate Research Fellowship
</p>
<p>
  2016-01-31:
  Congratulations to Philippe Kirschen and the rest of the 
  <a href="http://hyperloop.mit.edu/">MIT team</a>
  on
  <a href="http://www.wired.com/2016/02/mit-students-just-won-a-competition-to-design-a-hyperloop-pod/">winning</a>
  the SpaceX Hyperloop design competition
</p>
</div>
