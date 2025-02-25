---
layout: default
title: Home | Organization Name
---

<div class="container-fluid index-content-container">
  <h1 class="section-header">About Us</h1>
  <div class="row about-us-grid">
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

<div class="container-fluid index-content-container">
  <h1 class="section-header">Recent Projects</h1>
  <div class="project-grid landing-page-project-grid">
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
  <!-- <ul>
    {% for project in site.projects %}
      <li>
        <h2>{{ project.name }}</h2>
        <h3>{{ project.timeline }}</h3>
        <p>{{ project.content | markdownify }}</p>
      </li>
    {% endfor %}
  </ul> -->
  </div>
</div>

<div class="container-fluid index-content-container">
<h2>Recent papers</h2>
<ul>
  {% for paper in site.publications %}
    <li>
      <h2>{{ paper.title }}</h2>
    </li>
  {% endfor %}
</ul>
</div>

<div class="container-fluid index-content-container">
<h2>Sponsors</h2>
</div>