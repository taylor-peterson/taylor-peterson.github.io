---
layout: landing_page
title: Projects
permalink: /projects/
---

{% for project in site.projects %}
        {% capture show %}{{ show }}[![{{ project.title }}]({{ project.image_path }}){:height="200px"}]({{ project.url }}){% endcapture %}
{% endfor %}
{{ show }}
