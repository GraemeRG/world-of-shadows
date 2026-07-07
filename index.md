---
layout: default
title: Home
---

<h1>Welcome to the Shadows</h1>

<p>
  This is a quiet corner of the web for projects built in spare hours and
  thoughts set down before they fade — homebrew games, mobile experiments,
  and whatever else has been worth lingering over by candlelight.
</p>

<p>
  Wander through the <a href="{{ '/projects.html' | relative_url }}">Projects</a>
  for a look at what's been built, or settle into the
  <a href="{{ '/blog.html' | relative_url }}">Writings</a> for longer thoughts.
</p>

<span class="ornament">&#10086; &#10087; &#10086;</span>

<h2>Recently Stirring</h2>
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
