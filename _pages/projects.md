---
layout: page
permalink: /projects/
title: projects
description: "Projects that are finished or work in progress (wip)."
nav: true
nav_order: 3
display_categories: [wip, finished]
pagination:
    enabled: true
    collection: projects
    permalink: /page/:num/
---
{% for project in site.projects %}
    <div>
        <h2><a href="{{ project.url | relative_url }}">{{ project.title }}</a></h2>
        <p><strong>Date:</strong> {{ project.date }}</p>
        <p><strong>Description:</strong> {{ project.description }}</p>
    </div>
{% endfor %}

