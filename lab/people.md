---
title: People
permalink: /lab/people/
layout: default
---
<link rel="stylesheet" href="{{ '/lab/assets/css/lab.css' | relative_url }}">
<div class="lab-container">
  <div class="card-grid">
    {% assign members = site.people | sort: "order" %}
    {% for m in members %}
      <div class="card">
        {% if m.photo %}<img class="avatar" src="{{ m.photo | relative_url }}" alt="{{ m.name }}">{% endif %}
        <h3><a href="{{ m.url | relative_url }}">{{ m.name }}</a></h3>
        {% if m.role %}<p class="muted">{{ m.role }}</p>{% endif %}
      </div>
    {% endfor %}
  </div>
</div>
