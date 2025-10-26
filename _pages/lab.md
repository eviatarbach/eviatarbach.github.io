---
layout: default
permalink: /lab/
title: PANDDA Lab
nav: true
nav_order: 3
description: Predictability of the Atmosphere, Nonlinear Dynamics, and Data Assimilation (PANDDA) Lab
---

<img src="{{ site.baseurl }}/assets/img/pandda_logo.svg" style="(min-width: {{site.max_width}})" alt="PANDDA logo" />

We are the Predictability of the Atmosphere, Nonlinear Dynamics, and Data Assimilation (PANDDA) Lab at the University of Reading.

<hr>
<div class="post">
  <article>
{% for person in site.data.members %}
    {% if person.image %}
        <div class="profile float-right">
        <img src="{{ person.image | prepend: '/assets/img/' | prepend: site.baseurl | prepend: site.url }}" class="img-fluid z-depth-1 rounded" style="(min-width: {{site.max_width}}) {{ site.max_width | minus: 30 | times: 0.3}}px, (min-width: 576px) 30vw, 95vw" alt="Photo of {{person.name}}" />
        </div>
    {% endif %}
        <div class="clearfix">
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

        <p class="text-justify">{{person.description | markdownify}}</p>
        </div>
<hr>
{% endfor %}

{% if site.data.students %}
  <h2 id="students">Students</h2>
  {% for person in site.data.students %}
    {% if person.image %}
        <div class="profile float-right">
        <img src="{{ person.image | prepend: '/assets/img/' | prepend: site.baseurl | prepend: site.url }}" class="img-fluid z-depth-1 rounded" style="(min-width: {{site.max_width}}) {{ site.max_width | minus: 30 | times: 0.3}}px, (min-width: 576px) 30vw, 95vw" alt="Photo of {{person.name}}" />
        </div>
    {% endif %}
        <div class="clearfix">
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

        <p class="text-justify">{{person.description | markdownify}}</p>
        </div>
<hr>
  {% endfor %}
{% endif %}
  </article>
</div>

Logo designed by <a href="https://melissagoon.dev/">Melissa Goon</a>.
