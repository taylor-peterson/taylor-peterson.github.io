---
title: Musings
---

{% for musing in site.musings %}
# [{{ musing.title }}]({{ musing.url }})
{{ musing.excerpt }}
{% endfor %}
