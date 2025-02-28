---
layout: default
title: Test Page
date: 2020-01-01
start-date: 2020-01-01
end-date: 2023-01-01
---

{% assign var = "person-one" %}
{% assign items = site.people | where_exp: "record", "record.short-name contains var" %}
<p>items: {{items | inspect}}</p>


<p>{{ site.people | inspect }}</p>
<p>{{ site.people[0].id }}</p>
<p>lookup: {{ site.people[site.people[0].id] }}</p>
<p>{{ site.data.people["person-one"]}}</p>
<p>{{ site.collections.people | inspect }}</p>

<p>{{ site.data.nav-bar | inspect }}</p>
<p>{{ site.data.people | inspect }}</p>
{% for collection in site.collections %}
<h2> collection </h2>
<h3>{{collection.name}}</h3>
{{ collection | inspect }}
{% endfor %}

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