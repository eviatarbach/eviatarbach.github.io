---
layout: page
permalink: /publications/
title: Publications
description:
years: [2024, 2023, 2022, 2021, 2019, 2018]
nav: true
nav_order: 2
---
<!-- _pages/publications.md -->
See also my <a href="https://scholar.google.com/citations?user=qeCEIpwAAAAJ&hl=en">Google Scholar</a>. Asterisks (*) indicate papers on which I am the sole or co-first author, or the sole or co-corresponding author. Frequent collaborators have their websites linked in the author lists below.

<div class="publications">

<h2 class="year">Preprints</h2>

{% bibliography -f preprints %}

{% for y in page.years %}
  <h2 class="year">{{y}}</h2>
  {% bibliography -f papers -q @*[year={{y}}]* %}
{% endfor %}

</div>
