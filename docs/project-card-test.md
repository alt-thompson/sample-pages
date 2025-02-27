---
layout: default
title: Project Card Test Page
---

{% assign project = site.projects | first %}
{% include project-card.html project=project %}