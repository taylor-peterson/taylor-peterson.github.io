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

<style type="text/css">{% include timeline.css %}</style>

<ul class="timeline">
{% for project in site.projects %}
    <li>
        <div class="timeline-badge">
          <a><i class="fa fa-circle" id=""></i></a>
        </div>
        <div class="timeline-panel">
            <div class="timeline-heading">
            <h4><a href="{{project.url}}">{{ project.title }}</a></h4>
            </div>
            <div class="timeline-body">
{% assign image_path_base = "https://res.cloudinary.com/peterson/w_auto,c_scale,dpr_1.0,f_auto,q_auto/" %}
{% assign image_path_full = image_path_base | append: {{ project.image_path }} %}
{% include image.html
path=image_path_full
%}
            <p>{{project.summary}}</p>
            </div>
            <div class="timeline-footer">
                <p class="text-right">Feb-21-2014</p>
            </div>
        </div>
    </li>
{% endfor %}
    <li class="timeline-inverted">
        <div class="timeline-badge">
            <a><i class="fa fa-circle invert" id=""></i></a>
        </div>
        <div class="timeline-panel">
            <div class="timeline-heading">
                <h4>Timeline Event</h4>
            </div>
            <div class="timeline-body">
                <p>Stranguillione in deinde cepit roseo commendavit patris super color est se sed. Virginis plus plorantes abscederem assignato ipsum ait regem Ardalio nos filiae Hellenicus mihi cum. Theophilo litore in lucem in modo invenit quasi nomen magni ergo est se est Apollonius, habet clementiae venit ad nomine sed dominum depressit filia navem.</p>
            </div>
            <div class="timeline-footer">
                <p class="text-right">Feb-23-2014</p>
            </div>
        </div>
    </li>
    
    <li>
        <div class="timeline-badge">
            <a><i class="fa fa-circle" id=""></i></a>
        </div>
        <div class="timeline-panel">
            <div class="timeline-heading">
                <h4>Timeline Event</h4>
            </div>
            <div class="timeline-body">
                <p>Advenientibus aliorum eam ad per te sed. Facere debetur aut veneris accedens.</p>
            </div>
            <div class="timeline-footer">
                <p class="text-right">Feb-23-2014</p>
            </div>
        </div>
    </li>
    
    <li class="timeline-inverted">
        <div class="timeline-badge">
            <a><i class="fa fa-circle invert" id=""></i></a>
        </div>
        <div class="timeline-panel">
            <div class="timeline-heading">
                <h4>Timeline Event</h4>
            </div>
            <div class="timeline-body">
                <p>Volvitur ingreditur id ait mea vero cum autem quod ait Cumque ego illum vero cum unde beata. Commendavi si non dum est in. Dionysiadem tuos ratio puella ut casus, tunc lacrimas effunditis magister cives Tharsis. Puellae addita verbaque' capellam sanctissima quid, apollinem existimas filiam rex cum autem quod tamen adnuente rediens eam est se in. Peracta licet ad nomine Maria non ait in modo compungi mulierem volutpat.</p>
            </div>
            <div class="timeline-footer">
                <p class="text-right">Feb-27-2014</p>
            </div>
        </div>
    </li>
    
    <li>
        <div class="timeline-badge">
            <a><i class="fa fa-circle" id=""></i></a>
        </div>
        <div class="timeline-panel">
            <div class="timeline-heading">
                <h4>Timeline Event</h4>
            </div>
            <div class="timeline-body">
                <p>Adfertur guttae sapientiae ducitur est Apollonius ut a a his domino Lycoridem in lucem. Theophile atque bona dei cenam veniebant est cum. Iusto opes mihi Tyrum in modo compungi mulierem ubi augue eiusdem ordo quos vero diam omni catervis famulorum. Bene dictis ut diem finito servis unde.</p>
            </div>
            <div class="timeline-footer">
                <p class="text-right">Mar-01-2014</p>
            </div>
        </div>
    </li>
    
    <li  class="timeline-inverted">
        <div class="timeline-badge">
            <a><i class="fa fa-circle invert" id=""></i></a>
        </div>
        <div class="timeline-panel">
            <div class="timeline-heading">
                <h4>Timeline Event</h4>
            </div>
            <div class="timeline-body">
                <p>Crede respiciens loco dedit beneficio ad suis alteri si puella eius in. Acceptis codicello lenonem in deinde plectrum anni ipsa quod eam est Apollonius.</p>
            </div>
            <div class="timeline-footer primary">
                <p class="text-right">Mar-02-2014</p>
            </div>
        </div>
    </li>
    <li class="clearfix no-float"></li>
</ul>
