---
layout: default
title: Test Page
date: 2020-01-01
start-date: 2020-01-01
end-date: 
---

{% assign start_date = page.date | date: "%Y" %}
{{ page.date | date: "%Y" }}

{% capture timeline %} {{ page.start-date | date: "%Y" }} - {{ page.end-date | date: "%Y" | default: "Present" }} {% endcapture %}

{{ timeline }}