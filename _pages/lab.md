---
layout: default
permalink: /lab/
title: PANDDA Lab
description: Predictability of the Atmosphere, Nonlinear Dynamics, and Data Assimilation (PANDDA) Lab
---

![Image]({{ site.baseurl }}/assets/img/pandda_logo.svg)

We are the Predictability of the Atmosphere, Nonlinear Dynamics, and Data Assimilation (PANDDA) Lab at the University of Reading.

{% for person in site.data.members %}

<!-- The paddingtop and margin-top edits allow anchors to link properly. -->
<div id = "{{person.name | replace: ' ', '-'}}" class="row" style="padding-top: 60px; margin-top: -60px;">
    {% if person.image %}
        <div class="profile float-right">
        {% include figure.liquid loading="eager" path="{{ person.image | prepend: '/assets/img/' | prepend: site.baseurl | prepend: site.url }}" class="img-fluid z-depth-1 rounded" sizes="(min-width: {{site.max_width}}) {{ site.max_width | minus: 30 | times: 0.3}}px, (min-width: 576px) 30vw, 95vw" alt="Photo of {{person.name}}" %}
        </div>
    {% endif %}
    <div>
        <h4>{{person.name}}{% if person.degrees %}, {{person.degrees}} {% endif %}</h4> 
        {{person.position}} <br>
        {% if person.email %}
            <i class="fa fa-envelope"></i> <em>{{person.email}}</em> <br>
        {% endif %}
        {% if person.website %}
          <i class="fa fa-globe"></i> <a href= "{{person.website}}" target="_blank">{{person.website}}</a> <br>
        {% endif %}
        {% if person.github %}
          <i class="fab fa-github"></i> <a href= "https://github.com/{{person.github}}" target="_blank"> {{person.github}} </a> <br>
        {% endif %}
        {% if person.scholar %}
          <i class="ai ai-google-scholar"></i> <a href= "http://scholar.google.com/citations?user={{person.scholar}}" target="_blank"> Scholar Citations </a> <br>
        {% endif %}
        {% if person.orcid %}
          <i class="ai ai-orcid"></i> <a href="http://{{person.orcid}}" target="_blank"> {{person.orcid}}</a> <br>
        {% endif %}

    </div>
    <div class="col-sm-8">
        <p class="text-justify">{{person.description | markdownify}}</p>
    </div>
</div>
<hr>
{% endfor %}

{% if site.data.students %}
  <h2 id="students">Students</h2>
  {% for person in site.data.students %}
<div id = "{{person.name | replace: ' ', '-'}}" class="row" style="padding-top: 60px; margin-top: -60px;">
    {% if person.image %}
        <div class="profile float-right">
        {% capture sizes %}(min-width: {{site.max_width}}) {{ site.max_width | minus: 30 | times: 0.3}}px, (min-width: 576px) 30vw, 95vw"{% endcapture %}
        {% include figure.liquid loading="eager" path="{{ person.image | prepend: '/assets/img/' | prepend: site.baseurl | prepend: site.url }}" class="img-fluid z-depth-1 rounded" sizes=sizes alt="Photo of {{person.name}}" %}
        </div>
    {% endif %}
    <div>
        <h4>{{person.name}}{% if person.degrees %}, {{person.degrees}} {% endif %}</h4> 
        {{person.position}} <br>
        {% if person.email %}
            <i class="fa fa-envelope"></i> <em>{{person.email}}</em> <br>
        {% endif %}
        {% if person.website %}
          <i class="fa fa-globe"></i> <a href= "{{person.website}}" target="_blank">{{person.website}}</a> <br>
        {% endif %}
        {% if person.github %}
          <i class="fab fa-github"></i> <a href= "https://github.com/{{person.github}}" target="_blank"> {{person.github}} </a> <br>
        {% endif %}
        {% if person.scholar %}
          <i class="ai ai-google-scholar"></i> <a href= "http://scholar.google.com/citations?user={{person.scholar}}" target="_blank"> Scholar Citations </a> <br>
        {% endif %}
        {% if person.orcid %}
          <i class="ai ai-orcid"></i> <a href="http://{{person.orcid}}" target="_blank"> {{person.orcid}}</a> <br>
        {% endif %}

    </div>
    <div class="col-sm-8">
        <p class="text-justify">{{person.description | markdownify}}</p>
    </div>
</div>
<hr>
  {% endfor %}
{% endif %}

Logo designed by <a href="https://melissagoon.dev/">Melissa Goon</a>.
