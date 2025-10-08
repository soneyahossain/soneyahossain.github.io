---
title: Projects
permalink: /lab/projects/
layout: default
---
<link rel="stylesheet" href="{{ '/lab/assets/css/lab.css' | relative_url }}">
<div class="lab-container">
  <div class="card-grid">
    {% assign projects = site.projects | sort: "order" %}
    {% for p in projects %}
      <div class="card">
        <h3><a href="{{ p.url | relative_url }}">{{ p.title }}</a></h3>
        <p class="muted">{{ p.summary }}</p>
      </div>
    {% endfor %}
  </div>
</div>
