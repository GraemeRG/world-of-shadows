---
layout: default
title: Projects
---

<h1>Projects</h1>

<ul class="entry-list">
  {% assign projects = site.projects | sort: 'date' | reverse %}
  {% for project in projects %}
  <li>
    <h2 class="entry-title"><a href="{{ project.url | relative_url }}">{{ project.title }}</a></h2>
    {% if project.tagline %}<p class="entry-excerpt">{{ project.tagline }}</p>{% endif %}
    {% if project.stack %}
    <div class="project-stack">
      {% for item in project.stack %}<span>{{ item }}</span>{% endfor %}
    </div>
    {% endif %}
  </li>
  {% endfor %}
</ul>
