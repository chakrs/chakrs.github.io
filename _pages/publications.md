---
layout: page
permalink: /publications/
title: publications
#description: publications by categories in reversed chronological order.
years: [2025, 2023, 2022, 2021, 2005, 2004]
nav: true
nav_order: 2
---
<!-- _pages/publications.md -->
<div class="publications">
{%- for y in page.years %}
  <h2 class="year">{{y}}</h2>
  {% bibliography -f papers -q @*[year={{y}}]* %}
{% endfor %}

</div>
