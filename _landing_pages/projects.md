---
layout: projects
title: Projects
---

<link title="timeline-styles" rel="stylesheet" href="https://cdn.knightlab.com/libs/timeline3/latest/css/timeline.css">
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
    {
        "media": {
          "url": "https://res.cloudinary.com/peterson/w_auto,c_scale,dpr_1.0,f_auto,q_auto/projects/abetterpen/betterPenPrototype.png",
          "thumbnail": "https://res.cloudinary.com/peterson/w_auto,c_scale,dpr_1.0,f_auto,q_auto/gear.png",
          "caption": "Rendering of design.",
        },
        "start_date": {
          "year": "2013",
          "month": "12",
          "day": "23"
        },
        "end_date": {
          "year":"2015",
          "month": "5"
          },
        "text": {
           "headline": "<a href='abetterpen'>A Better Pen</a>",
          "text": "I'm a pen snob. Here's what I did about that."
        }
      }
      ]
};
var options = {
    autolink: false
}
  window.timeline = new TL.Timeline('timeline-embed', timeline_json, options)
</script>

<!-- The contents of this for-loop cannot be indented or the comments in image.html
     will be displayed as code in the generated output. --!>
{% for project in site.projects %}
{% assign image_path = project.image_path %}
<a href="{{ project.url }}">
{% include image.html
    path=image_path
%}
</a>
{% endfor %}
