---
layout: page
permalink: /publications/
title: publications
description: A list of my recent works.
years: [2023, 2022, 2021]
nav: true
nav_order: 1
bibtex_show: true
---
<!-- _pages/publications.md -->
<div class="publications">

{%- for y in page.years %}
  <h2 class="year">{{y}}</h2>
  {% bibliography -f papers -q @*[year={{y}}]* %}
{% endfor %}

</div>
