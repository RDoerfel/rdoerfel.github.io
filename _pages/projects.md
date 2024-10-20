---
layout: page
permalink: /projects/
title: projects
description: "Projects"
nav: true
nav_order: 3
---
{% for project in site.projects %}
  <h2>{{ project.title }} - {{ project.data }}</h2>
  <p>{{ project.description | markdownify }}</p>
{% endfor %}