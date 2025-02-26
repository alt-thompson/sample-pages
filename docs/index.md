---
layout: default
title: Home | Organization Name
---

<div class="container-fluid">
  <h1 class="section-header">About Us</h1>
  <div class="row">
    <div class="col-md-6 center-canvas">
      <!-- TODO: What is canvas? -->
      <canvas id="logo-canvas"></canvas>
    </div>
    <div class="col-md-6">
      <p>
        Information about our organization.
      </p>
    </div>
  </div>
</div>

{% include card-grid.html section="projects" %}
{% include card-grid.html section="publications" %}

<!-- <div class="container-fluid">
  <h1 class="section-header">Recent Projects</h1>
  <div class="project-grid">
  {% for project in site.projects %}
    <div class="project-card">
      <div class="project-image">
        Image
      </div>
      <div class="project-info">
        <p class="artifact-title line-clamp-one-line"> {{ project.name }} </p>
        <p class="artifact-title line-clamp-one-line">{{ project.timeline }}</p>
        <p>{{ project.content | markdownify }}</p>
      </div>
    </div>
  {% endfor %}
  </div>
</div> -->

<!-- <div class="container-fluid">
  <h1 class="section-header">Recent Papers</h1>
  <ul>
    {% for paper in site.publications %}
      <li>
        <h2>{{ paper.title }}</h2>
      </li>
    {% endfor %}
  </ul>
</div>

<div class="container-fluid">
  <h1 class="section-header">Sponsors</h1>
</div> -->