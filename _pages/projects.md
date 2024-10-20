---
layout: page
title: My Projects
permalink: /projects/
nav: true
nav_order: 3
---

{% for project in site.projects %}
### [{{ project.title }}]({{ project.url }})

**Category:** {{ project.category }}

**Date:** {{ project.date }}

{{ project.description }}
{% endfor %}