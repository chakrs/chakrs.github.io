---
layout: reviewer
permalink: /reviewer/
title: reviewer
description: Professional conference and books for which I have reviewed submissions
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
