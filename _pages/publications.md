---
layout: page
permalink: /publications/
title: Publications
description:
nav: true
nav_order: 2
---

<!-- _pages/publications.md -->

<!-- Bibsearch Feature -->

{% include bib_search.liquid %}

<style>
  :root {
    --global-theme-color: #009c8c;
    --global-hover-color: #007f73;
  }

  html[data-theme="dark"] {
    --global-theme-color: #4db6ac;
    --global-hover-color: #80cbc4;
  }

  .publications .author em {
    font-style: normal;
    font-weight: 700;
  }
</style>

<div class="publications">

{% bibliography %}

</div>
