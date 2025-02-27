---
layout: default
title: Project Card Test Page
---

Hello
{% assign first_project = site.projects | first %}
<p> First project: '{{ first_project }}' </p>
{% include project-card.html project=first_project %}