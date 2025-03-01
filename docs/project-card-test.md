---
layout: default
title: Paper Card Test Page
---

{% assign paper = site.publications | first %}
{% include paper-card.html paper=paper %}