---
layout: default
permalink: /lab/
title: PANDDA Lab
description: Predictability of the Atmosphere, Nonlinear Dynamics, and Data Assimilation (PANDDA) Lab
profiles:
  - name: Eviatar Bach
    align: right
    image: eviatar_bach.jpg
    content: Principal Investigator
    image_circular: false # crops the image to make it circular
    more_info:
---

![Image]({{ site.baseurl }}/assets/img/pandda_logo.svg)

We are the Predictability of the Atmosphere, Nonlinear Dynamics, and Data Assimilation (PANDDA) Lab at the University of Reading.

<div class="post">
  <article>
    {% if page.profiles %}
      {% for profile in page.profiles %}
        <hr>
        <div class="profile float-{% if profile.align == 'left' %}left{% else %}right{% endif %}">
          {% if profile.image %}
            {% assign profile_image_path = profile.image | prepend: 'assets/img/' %}
            {% if profile.image_circular %}
              {% assign profile_image_class = 'img-fluid z-depth-1 rounded-circle' %}
            {% else %}
              {% assign profile_image_class = 'img-fluid z-depth-1 rounded' %}
            {% endif %}
            {% capture sizes %}(min-width: {{site.max_width}}) {{ site.max_width | minus: 30 | times: 0.3}}px, (min-width: 576px) 30vw, 95vw"{% endcapture %}
            {% include figure.liquid loading="eager" path=profile_image_path class=profile_image_class sizes=sizes alt=profile.image %}
          {% endif %}
          {% if profile.more_info %}
            <div class="more-info">{{ profile.more_info }}</div>
          {% endif %}
        </div>

        <div class="clearfix">
          <h4>{% profile.name %}</h4>
          {% if profile.content %}
            {{ profile.content | markdownify }}
          {% endif %}
        </div>
      {% endfor %}
    {% endif %}
  </article>
</div>

Logo designed by <a href="https://melissagoon.dev/">Melissa Goon</a>.
