---
layout: page
permalink: /publications/
title: publications
description:
years: [2022, 2021, 2019, 2018]
nav: true
nav_order: 2
---
<!-- _pages/publications.md -->
<div class="publications">

<h3 class="year">Preprints/in press</h3>
{% bibliography -f preprints %}

{% for y in page.years %}
  <h3 class="year">{{y}}</h3>
  {% bibliography -f papers -q @*[year={{y}}]* %}
{% endfor %}

</div>
