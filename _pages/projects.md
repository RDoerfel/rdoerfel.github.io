---
layout: page
title: My Projects
permalink: /projects/
---

{% for project in site.projects %}
- [{{ project.title }}]({{ project.url }})
  {{ project.description }}
{% endfor %}