---
layout: page
title: projects
description: "A list of projects I have worked on."
permalink: /projects/
nav: true
nav_order: 3
---

{% for project in site.projects %}
### [{{ project.title }}]({{ project.url }})

**Category:** {{ project.category }}  
**Date:** {{ project.date  | date: "%B %d, %Y"}}

{{ project.description }}
{% endfor %}