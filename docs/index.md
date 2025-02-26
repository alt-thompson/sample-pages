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

{% include card-grid.html section="projects" values=site.projects %}
{% include card-grid.html section="publications" values=site.publications %}
