---
layout: projects
title: Projects
---

<link title="timeline-styles"
      rel="stylesheet"
      href="https://cdn.knightlab.com/libs/timeline3/latest/css/timeline.css">
<script src="https://cdn.knightlab.com/libs/timeline3/latest/js/timeline.js"></script>

<div id='timeline-embed' style="width: 100%; height: 600px"></div>

<script type="text/javascript">
var timeline_json = {
    "title": {
        "text": {
          "headline": "Awesome Stuff Taylor's Done",
          "text": "Explore the detail pages for more info!"
        }
    },
    "events": [
{% for project in site.projects %}
    {
        "media": {
            "url": "https://res.cloudinary.com/peterson/w_auto,c_scale,dpr_1.0,f_auto,q_auto/{{ project.image_path }}",
            "thumbnail": "https://res.cloudinary.com/peterson/w_auto,c_scale,dpr_1.0,f_auto,q_auto/gear.png",
        },
        "start_date": {
            "year": "{{ project.start_date[0] }}",
            "month": "{{ project.start_date[1] }}",
            "day": "{{ project.start_date[2] }}"
        },
        "end_date": {
            "year": "{{ project.end_date[0] }}",
            "month": "{{ project.end_date[1] }}",
            "day": "{{ project.end_date[2] }}"
          },
        "text": {
            "headline": "<a href='{{ project.url }}'>{{ project.title }}</a>",
            "text": "{{ project.summary }}"
        }
      },
{% endfor %}
      ]
};
  window.timeline = new TL.Timeline('timeline-embed', timeline_json)
</script>
