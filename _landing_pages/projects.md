---
layout: landing_page
title: Projects
permalink: /projects/
---

{% capture hide %}
{% for project in site.projects %}
    {% assign project_url_parts = project.url | split: '/' %}
    {% assign project_url_parts_size = project_url_parts | size %}
    {% if project_url_parts_size == 3 or project.path contains 'index' %}
        {% capture show %}{{ show }}[![{{ project.title }}]({{ project.image_path }}){:height="200px"}]({{ project.url }}){% endcapture %}
    {% endif %}
{% endfor %}
{% endcapture %}
{{ show }}
