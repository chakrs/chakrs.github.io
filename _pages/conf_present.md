---
layout: conf_present
permalink: /conf_present/
title: conference presentations
description: I'm thrilled to share that I've been actively engaged in submitting my research findings and eagerly presenting them at various prestigious conferences. Below, you'll find the list of conferences where I've had the privilege to showcase my work.
nav: false
nav_order: 2
---
<table>
  {% for row in site.data.conf_present %}
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
