---
layout: page
permalink: /publications/
title: Publications
description:
years: [2022, 2021, 2019, 2018]
nav: true
nav_order: 2
---
<script type='text/javascript' src='https://d1bxh8uas1mnw7.cloudfront.net/assets/embed.js'></script>

<!-- _pages/publications.md -->
<div class="publications">

<h2 class="year">Preprints</h2>
{% bibliography -f preprints %}

{% for y in page.years %}
  <h2 class="year">{{y}}</h2>
  {% bibliography -f papers -q @*[year={{y}}]* %}
{% endfor %}

</div>
