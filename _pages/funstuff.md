---
layout: table
permalink: /funstuff/
title: funstuff
description: Half Marathons
nav: false
nav_order: 5
---

<table>
  {% for row in site.data.half_marathons %}
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
