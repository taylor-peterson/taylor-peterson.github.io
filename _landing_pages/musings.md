---
layout: default
title: Musings
permalink: /musings/
---

{% for musing in site.musings %}
    {% assign musing_url_parts = musing.url | split: '/' %}
    {% assign musing_url_parts_size = musing_url_parts | size %}
    {% if musing_url_parts_size == 3 or musing.path contains 'index' %}
# [{{ musing.title }}]({{ musing.url }})
{{ musing.excerpt }}
    {% endif %}
{% endfor %}
