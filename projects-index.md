---
layout: default
title: Projects
---

{% for project in site.projects %}
# [{{ project.title }}]({{ project.url }})
[![{{ project.title }}]({{ project.image_path }})]({{ project.url }})
{% endfor %}
