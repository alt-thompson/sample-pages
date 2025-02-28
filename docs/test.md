---
layout: default
title: Test Page
date: 2020-01-01
start-date: 2020-01-01
end-date: 2023-01-01
---

{% assign person-id = "person-one" %}
{{ person-id }}
<!-- {{ site.people | where_exp: "item", "item.short-name == 'person-one'" }} -->

<p>{{ site.people | map: "url" }}</p>
{{ site.people | where: "short-name", "person-one" | map: "url" }}
{% assign project-one-lead-id = site.projects | where: "short-name", "project-one" | map: "lead" %}
<p><b>Lead Id: </b>{{project-one-lead-id}}</p>
{% assign project-one-lead = site.people | where_exp: "item", "item.short-name == project-one-lead-id" %}
<p><b>Lead: </b>{{ project-one-lead }}</p>
<p><b>Lead URL: </b>{{project-one-lead.url | relative_url}}</p>

{% assign start_date = page.date | date: "%Y" %}
{{ page.date | date: "%Y" }}

{% capture timeline %} {{ page.start-date | date: "%Y" }} - {{ page.end-date | date: "%Y" | default: "Present" }} {% endcapture %}

{{ timeline }}