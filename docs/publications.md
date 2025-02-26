---
layout: default
title: Publications
---

<ul>
  {% for paper in site.publications %}
    <li>
      <h2>{{ paper.title }}</h2>
      <h3>{{ paper.authors }}</h3>
      <p>{{ paper.content | markdownify }}</p>
    </li>
  {% endfor %}
</ul>