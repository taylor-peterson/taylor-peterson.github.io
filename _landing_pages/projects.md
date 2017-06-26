---
layout: projects
title: Projects
---

<ul class="projects">
{% assign projects = site.projects | sort: 'end_date' | reverse %}
{% for post in projects %}
  <div class="col-md-6 col-sm-12">
  <li>
    <div class="project">
      <a class="cover" href="{{ post.url }}">
        <div class="project-details">
          <span> {{ post.title }} </span>
          <span> {{ post.summary }} </span>
        </div>
      </a>
      <img class="thumb" src="https://res.cloudinary.com/peterson/w_auto:100:400,c_scale,dpr_auto,f_auto,q_auto/{{ post.image_path }}" />
      <div class="aspect-two-one"></div>
    </div>
  </li>
    </div>
{% endfor %}
</ul>
