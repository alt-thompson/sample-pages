---
layout: default
title: Paper Card Test Page
---

{% assign paper = site.publications | first %}

{% include paper-grid.html header="Publications" values=site.publications %}