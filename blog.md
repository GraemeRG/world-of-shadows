---
layout: default
title: Writings
---

<h1>Writings</h1>

<ul class="entry-list">
  {% for post in site.posts %}
  <li>
    <h2 class="entry-title"><a href="{{ post.url | relative_url }}">{{ post.title }}</a></h2>
    <div class="entry-meta">
      {{ post.date | date: "%-d %B %Y" }}
      {% if post.tags.size > 0 %}
        &middot;
        {% for tag in post.tags %}<span class="tag">{{ tag }}</span>{% endfor %}
      {% endif %}
    </div>
    <p class="entry-excerpt">{{ post.excerpt | strip_html | truncate: 160 }}</p>
  </li>
  {% endfor %}
</ul>
