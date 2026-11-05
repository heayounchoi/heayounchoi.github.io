---
layout: page
title: Projects
permalink: /projects/
description:
nav: true
nav_order: 3
display_categories: [research]
horizontal: false
---

<style>
  :root {
    --global-theme-color: #009c8c;
    --global-hover-color: #007f73;
  }

  html[data-theme="dark"] {
    --global-theme-color: #4db6ac;
    --global-hover-color: #80cbc4;
  }
</style>

<div class="publications">
  <ol class="bibliography">
    {% assign research_projects = site.projects | where: "category", "research" | sort: "importance" %}
    {% for project in research_projects %}
      <li>
        <div class="row">
          <div class="col col-sm-2 abbr">
            {% if project.img %}
              {% include figure.liquid loading="eager" path=project.img sizes="200px" class="preview z-depth-1 rounded" alt=project.title %}
            {% endif %}
          </div>
          <div class="col-sm-8">
            <div class="title">{{ project.title }}</div>
            <div class="author">{{ project.description }}</div>
            <div class="periodical">Funded by the {{ project.funding }}.</div>
          </div>
          <div class="col-sm-2">{{ project.year }}</div>
        </div>
      </li>
    {% endfor %}
  </ol>
</div>
