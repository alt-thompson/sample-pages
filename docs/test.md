---
layout: default
title: Test Page
---

<ul>
  {% for project in site.projects limit:3 %}
    <li>
      <p>{{ project.name }}</p>
      <p>{{ project.timeline }}</p>
      <p>{{ project.content | markdownify }}</p>
    </li>
  {% endfor %}
</ul>