---
layout: default
title: Home
---

The goal of our research is more reliable and efficient ways to design engineering systems. To accomplish this, we draw heavily on mathematical tools from convex optimization. One product of our group's work is <a href="http://gpkit.readthedocs.io/en/latest/">GPkit</a>, a software package for geometric programming.
<br>

<iframe width="560" height="315" src="https://www.youtube.com/embed/HMu3x5WxpeM" frameborder="0" allowfullscreen></iframe>
First flight of the Jungle Hawk Owl 5-day endurance UAV, designed using GPkit. <a href="http://news.mit.edu/2017/drones-stay-aloft-five-days-0607">MIT News article</a>


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
  2017-05-25:
  Congratulations to Martin York on submitting his Master's thesis on <a href ="/publications/york_masters_thesis.pdf"> Turbofan Engine Sizing and Tradeoff Analysis via Signomial Programming</a>. 
</p>
<p>
  2017-05-25:
  Congratulations to Cody Karcher on submitting his Master's thesis on <a href ="/publications/karcher_masters_thesis.pdf"> A Heuristic for Including Black Box Analysis Tools into a Geometric Programming Formulation</a>. 
</p>
<p>
  2016-12-29:
  Congratulations to Martin York on being named <a href="http://news.mit.edu/2016/martin-york-named-us-air-force-cadet-of-the-year-1229">United States Air Force Cadet of the year</a>.
</p>
<p>
  2016-03-29:
  Congratulations to Mike Burton on winning an NSF Graduate Research Fellowship.
</p>
<p>
  2016-01-31:
  Congratulations to Philippe Kirschen and the rest of the 
  <a href="http://hyperloop.mit.edu/">MIT team</a>
  on
  <a href="http://www.wired.com/2016/02/mit-students-just-won-a-competition-to-design-a-hyperloop-pod/">winning</a>
  the SpaceX Hyperloop design competition.
</p>
</div>
