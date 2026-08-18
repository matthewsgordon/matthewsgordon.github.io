---
layout: page
title: Projects
permalink: /projects/
---

My projects and publications.

{% if site.projects %}
## Publications

<ul class="publication-list">
{% for item in site.projects %}
  {% if item.type == "publication" %}
  <li>
    <h3><a href="{{ item.link }}">{{ item.title }}</a></h3>
    <p>{{ item.authors }} — <em>{{ item.venue }}</em>, {{ item.year }}</p>
    {% if item.abstract %}<p>{{ item.abstract }}</p>{% endif %}
  </li>
  {% endif %}
{% endfor %}
</ul>
{% endif %}

{% if site.projects %}
## Projects

<ul class="project-list">
{% for item in site.projects %}
  {% if item.type == "project" %}
  <li>
    <h3><a href="{{ item.link }}">{{ item.title }}</a></h3>
    <p>{{ item.description }}</p>
  </li>
  {% endif %}
{% endfor %}
</ul>
{% endif %}