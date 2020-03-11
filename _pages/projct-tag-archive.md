---
title: Projects by Tag
permalink: "/project-tags/"
collection: projects
layout: archive
pagination:
  enabled: true
  collection: all
  permalink: /:num/
author_profile: true
---


{% assign tags =  site.projects | map: 'tags' | uniq %}
{% for tag in tags %}
  <h3>{{ tag }}</h3>
  <ul>
  {% for note in site.projects %}
    {% if note.tags contains tag %}
    <li><a href="{{ site.baseurl }}{{ note.url }}">{{ note.title }}</a></li>
    {% endif %}
  {% endfor %}
  </ul>
{% endfor %}
