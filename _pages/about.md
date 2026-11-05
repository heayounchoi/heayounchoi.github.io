---
layout: about
title: About
permalink: /
subtitle:

profile:
  align: right
  image: heayoun-choi.jpg
  image_circular: false

selected_papers: false
social: false

announcements:
  enabled: false # enable after adding current news items
  scrollable: true # adds a vertical scroll bar if there are more than 3 news items
  limit: 5 # leave blank to include all the news in the `_news` folder

latest_posts:
  enabled: false
  scrollable: true # adds a vertical scroll bar if there are more than 3 new posts items
  limit: 3 # leave blank to include all the blog posts
---

<div class="contact-icons" style="text-align: left; margin: -0.75rem 0 1.25rem">
  <a href="mailto:heayounchoi@gmail.com" title="Email"><i class="fa-solid fa-envelope"></i></a>
  <a href="https://github.com/heayounchoi" title="GitHub"><i class="fa-brands fa-github"></i></a>
  <a href="https://scholar.google.com/citations?user=IoJi1pEAAAAJ" title="Google Scholar"><i class="ai ai-google-scholar"></i></a>
</div>

I am a **Research Intern** at the University of Toronto's [Medical Computer Vision and Robotics (MEDCVR) Lab](https://medcvr.utm.utoronto.ca/), advised by Professor [Lueder A. Kahrs](https://www.utm.utoronto.ca/math-cs-stats/people/lueder-kahrs). I received my M.S. in Computer Science & Engineering from Chung-Ang University, advised by Professor [Eunwoo Kim](https://airlab.cau.ac.kr/members/professor/) at the [AI and Robotics Lab](https://airlab.cau.ac.kr/).

My research focuses on **generalization, autonomous adaptation, and physical-world reasoning** for robots operating in changing and unfamiliar environments, with a long-term interest in autonomous exploration and sustainable habitats beyond Earth.

## News

- **2026.10** — Our paper on VLA model adaptation was accepted to RA-L.
- **2026.10** — Joined the MEDCVR Lab at the University of Toronto as a Research Intern.
- **2026.10** — Named a Top Reviewer as a NeurIPS 2026 main-track reviewer.
- **2026.08** — Received my M.S. in Computer Science & Engineering from Chung-Ang University.
- **2026.01** — My first-author paper on continual generalization was accepted to ICLR 2026. See you in Brazil!

## Publications

<style>
  .profile img {
    aspect-ratio: 4 / 5;
    object-fit: cover;
    object-position: center 35%;
  }

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

## Projects

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
