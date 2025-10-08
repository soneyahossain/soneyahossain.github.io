---
title: News
permalink: /lab/news/
layout: default
---
<link rel="stylesheet" href="{{ '/lab/assets/css/lab.css' | relative_url }}">
<div class="lab-container">
  {% assign items = site.news | sort: "date" | reverse %}
  {% for n in items %}
    <div class="news-item">
      <p class="muted">{{ n.date | date: "%b %e, %Y" }}</p>
      <h3><a href="{{ n.url | relative_url }}">{{ n.title }}</a></h3>
      <p>{{ n.excerpt | strip_html }}</p>
    </div>
  {% endfor %}
</div>
