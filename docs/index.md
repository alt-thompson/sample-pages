---
layout: default
title: Home | Organization Name
---

<div>
Information about our organization
</div>

<div>
<h2>Recent projects</h2>
<ul>
  {% for project in site.projects %}
    <li>
      <h2>{{ project.name }}</h2>
      <h3>{{ project.timeline }}</h3>
      <p>{{ project.content | markdownify }}</p>
    </li>
  {% endfor %}
</ul>
</div>

<div>
<h2>Recent papers</h2>
<ul>
  {% for paper in site.publications %}
    <li>
      <h2>{{ paper.title }}</h2>
    </li>
  {% endfor %}
</ul>
</div>

<div>
<h2>Sponsors</h2>
</div>