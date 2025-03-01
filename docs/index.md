---
layout: default
title: Home | Organization Name
---

{% include about.html %}
{% include project-grid-landing.html header="Recent Projects" values=site.projects %}

{% comment %} TODO: Replace below with better grids {% endcomment %}
{% include card-grid.html section="projects" values=site.projects %}
{% include card-grid.html section="publications" values=site.publications %}
