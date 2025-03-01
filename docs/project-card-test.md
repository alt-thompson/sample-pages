---
layout: default
title: Project Card Test Page
---

{% assign member = site.people | first %}
{% include member-card.html member=member %}