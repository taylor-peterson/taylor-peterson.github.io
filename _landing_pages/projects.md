---
layout: projects
title: Projects
---

{% for project in site.projects %}
        {% capture show %}{{ show }}[![{{ project.title }}](https://res.cloudinary.com/peterson/w_auto:100:400,c_scale,dpr_auto,f_auto,q_auto/{{ project.image_path }}){:height="200px"}]({{ project.url }}){% endcapture %}
{% endfor %}
{{ show }}
