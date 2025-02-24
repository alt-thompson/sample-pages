---
layout: default
title: Projects
---

<ul>
  {% for project in site.projects %}
    <li>
      <h2>{{ project.name }}</h2>
      <h3>{{ project.timeline }}</h3>
      <p>{{ project.content | markdownify }}</p>
    </li>
  {% endfor %}
</ul>