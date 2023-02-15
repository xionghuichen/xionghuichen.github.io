---
layout: page
permalink: /publications/
title: Publications
description: 
years: [2023, 2022, 2021, 2020, 2019]
nav: true
---
\* indicates equal contributioncon.

#### Preprints

<div class="publications">
{% for y in page.years %}
  {% bibliography -f preprint -q @*[year={{y}}]* %}
{% endfor %}
</div>

#### Papers

<div class="publications">

{% for y in page.years %}

<div>{{y}}</div>
  {% bibliography -f pubs -q @*[year={{y}}]* %}
{% endfor %}

</div>
