---
title: Publications
permalink: /lab/publications/
layout: default
---
<link rel="stylesheet" href="{{ '/lab/assets/css/lab.css' | relative_url }}">
<div class="lab-container">
  {% assign pubs = site.publications | sort: "year" | reverse %}
  {% for p in pubs %}
  <div class="news-item">
    <strong><a href="{{ p.url | relative_url }}">{{ p.title }}</a></strong><br>
    {{ p.authors | join: ", " }}. <em>{{ p.venue }}</em>{% if p.year %} ({{ p.year }}){% endif %}.
    {% if p.pdf %} [<a href="{{ p.pdf | relative_url }}">PDF</a>]{% endif %}
    {% if p.code %} [<a href="{{ p.code }}" target="_blank" rel="noopener">Code</a>]{% endif %}
  </div>
  {% endfor %}
</div>
