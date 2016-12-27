---
layout: default
title: Projects
---

{% for project in site.projects %}
    {% assign project_url_parts = project.url | split: '/' %}
    {% assign project_url_parts_size = project_url_parts | size %}
    {% if project_url_parts_size == 3 or project.path contains 'index' %}
# [{{ project.title }}]({{ project.url }})
{{ project.date }}

[![{{ project.title }}]({{ project.image_path }})]({{ project.url }})
    {% endif %}
{% endfor %}
