---
title: ASSERT Lab
permalink: /lab/
layout: default
---
<link rel="stylesheet" href="{{ '/lab/assets/css/lab.css' | relative_url }}">

<section class="hero">
  <div class="wrap">
    <p class="muted">AI for Software Engineering</p>
    <h1>ASSERT Lab</h1>
    <p class="lead">
      We combine program analysis and machine learning to automate testing, debugging, and repair—
      making software more reliable and development more cost-efficient.
    </p>
    <div class="actions">
      <a class="button primary" href="{{ '/lab/projects/' | relative_url }}">Explore Projects</a>
      <a class="button" href="{{ '/lab/publications/' | relative_url }}">Read Publications</a>
      <a class="button" href="{{ '/lab/people/' | relative_url }}">Meet the Team</a>
    </div>
  </div>
</section>

<section class="section">
  <div class="lab-container">
    <h2>Latest news</h2>
    <div class="card-grid">
      {% assign latest = site.news | sort: "date" | reverse | slice: 0,3 %}
      {% for item in latest %}
      <div class="card">
        <h3><a href="{{ item.url | relative_url }}">{{ item.title }}</a></h3>
        <p class="muted">{{ item.date | date: "%b %e, %Y" }}</p>
        <p>{{ item.excerpt | strip_html | truncate: 140 }}</p>
      </div>
      {% endfor %}
    </div>
  </div>
</section>

<section class="section">
  <div class="lab-container">
    <h2>Featured projects</h2>
    <div class="card-grid">
      {% assign featured = site.projects | where: "featured", true | slice: 0,3 %}
      {% for p in featured %}
      <div class="card">
        <h3><a href="{{ p.url | relative_url }}">{{ p.title }}</a></h3>
        <p class="muted">{{ p.summary }}</p>
      </div>
      {% endfor %}
    </div>
  </div>
</section>
