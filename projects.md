---
layout: default
title: Projects
permalink: /projects/
---

{% for project in site.projects %}
    {% assign project_url_parts = project.url | split: '/' %}
    {% assign project_url_parts_size = project_url_parts | size %}
    {% if project_url_parts_size == 3 or project.path contains 'index' %}
# [{{ project.title }}]({{ project.url }})
{{ project.dates }}

[![{{ project.title }}]({{ project.image_path }}){:height="200px"}]({{ project.url }})
    {% endif %}
{% endfor %}
