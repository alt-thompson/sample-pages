---
layout: default
title: Test Page
date: 2020-01-01
start-date: 2020-01-01
end-date: 2023-01-01
---

{% assign var = "person-one" %}
{% assign items = site.people | where_exp: "record", "record.slug == var" %}
<p>items: {{ items | inspect }}</p>

<p>{{ site.people | inspect }}</p>
<p>{{ site.data.people["person-one"]}}</p>

<p>{{ site.data.nav-bar | inspect }}</p>
<p>{{ site.data.people | inspect }}</p>

{% assign start_date = page.date | date: "%Y" %}
{{ page.date | date: "%Y" }}

{% capture timeline %} {{ page.start-date | date: "%Y" }} - {{ page.end-date | date: "%Y" | default: "Present" }} {% endcapture %}

{{ timeline }}