---
layout: page
permalink: /publications/
title: Publications
description: publications by categories in reversed chronological order. generated by jekyll-scholar.
nav: true
nav_order: 2
---
<!-- _pages/publications.md -->
<div class="publications">

<!-- {% bibliography -f {{ site.scholar.bibliography }} %} -->

<h1>preprints</h1>

{% bibliography -f preprints %}

<h1>conference &amp; journal articles</h1>

{% for y in page.years %}
  <h2 class="year">{{y}}</h2>
  {% bibliography -f papers -q @*[year={{y}}]* %}
{% endfor %}

<h1>technical reports &amp; short papers</h1>

{% bibliography -f reports %}

</div>
