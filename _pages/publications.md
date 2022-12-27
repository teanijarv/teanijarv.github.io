---
layout: page
permalink: /publications/
title: publications
description: journal articles, conference papers and posters, and theses.
years_articles: [2023]
years_conferences: [2022, 2020]
years_theses: [2023, 2020]
nav: true
nav_order: 1
---
<!-- _pages/publications.md -->
<div class="publications">

<h1>journal articles</h1>

{%- for y in page.years_articles %}
  <h2 class="year">{{y}}</h2>
  {% bibliography -f articles -q @*[year={{y}}]* %}
{% endfor %}

<h1>conference papers and posters</h1>

{%- for y in page.years_conferences %}
  <h2 class="year">{{y}}</h2>
  {% bibliography -f conferences -q @*[year={{y}}]* %}
{% endfor %}

<h1>theses</h1>

{%- for y in page.years_theses %}
  <h2 class="year">{{y}}</h2>
  {% bibliography -f theses -q @*[year={{y}}]* %}
{% endfor %}

</div>
