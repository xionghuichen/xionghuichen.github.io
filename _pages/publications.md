---
layout: page
permalink: /publications/
title: Publications
description: 
years: [2026, 2025, 2024, 2023, 2022, 2021, 2020, 2019]
nav: true
---
\* indicates equal contribution; &dagger; indicates corresponding author; &sect; indicates project lead.

#### Preprints and Technical Reports

<div class="publications">
{% for y in page.years %}
  {% bibliography -f preprint -q @*[year={{y}}]* %}
{% endfor %}
</div>

#### Journal Articles

<div class="publications">
{% bibliography -f manus %}
</div>

#### Conference Papers

<div class="publications">

{% for y in page.years %}

{% capture paper_count %}{% bibliography_count -f pubs -q @*[year={{y}}]* %}{% endcapture %}
{% assign paper_count = paper_count | plus: 0 %}
{% if paper_count > 0 %}
<div>{{y}}</div>
  {% bibliography -f pubs -q @*[year={{y}}]* %}
{% endif %}
{% endfor %}

</div>
