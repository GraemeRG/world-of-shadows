---
layout: default
title: Home
---

<h1>We are the Shadows beneath Neon lights</h1>

<p>
  Welcome to the world of the shadows. This is my little corner of the internet, a showcase for projects anchored in my own little universe, Shadows Beneath Neon Lights.
</p>

<p>
  When I have them I'll be updating any released <a href="{{ '/projects.html' | relative_url }}">Projects</a> here
  and writing some less... strucutred... content 
  <a href="{{ '/blog.html' | relative_url }}">here</a>.
</p>

<h2>Recent posts</h2>
<ul class="entry-list">
  {% assign recent = site.posts | concat: site.projects | sort: 'date' | reverse %}
  {% for item in recent limit: 4 %}
  <li>
    <h3 class="entry-title"><a href="{{ item.url | relative_url }}">{{ item.title }}</a></h3>
    <div class="entry-meta">{{ item.date | date: "%-d %B %Y" }}</div>
    <p class="entry-excerpt">{{ item.excerpt | strip_html | truncate: 140 }}</p>
  </li>
  {% endfor %}
</ul>
