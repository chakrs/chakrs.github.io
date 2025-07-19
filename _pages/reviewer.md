---
layout: reviewer
permalink: /reviewer/
title: reviewer
description: I serve as a reviewer for submissions to professional conferences and academic publications, contributing my expertise to uphold quality and rigor in the field. Below are the conferences and books for which I have participated in the peer review process, helping to evaluate and select high-quality contributions in my area of specialization.

nav: false
nav_order: 2
---
<table>
  {% for row in site.data.reviewer %}
    {% if forloop.first %}
    <tr>
      {% for pair in row %}
        <th>{{ pair[0] }}</th>
      {% endfor %}
    </tr>
    {% endif %}

    {% tablerow pair in row %}
      {{ pair[1] }}
    {% endtablerow %}
  {% endfor %}
</table>
