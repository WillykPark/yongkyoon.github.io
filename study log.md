---
layout: list
title: Study Log
show_collection: study log
description: >
  This is the Study Log for remembering and sharing the knowledge about Robotics, Machine / Deep / Reingforcement Learning.
no_groups: true
---

## 🧠 Paper Review

{% assign papers = site.paper_review | sort: 'date' | reverse %}
<div class="projects">
  {% for item in papers limit:3 %}
  <article class="project">
    {% if item.image %}
    <div class="project-image">
      <img src="{{ item.image.path | relative_url }}" alt="{{ item.title }}">
    </div>
    {% endif %}
    <div class="project-title">
      <a href="{{ item.url }}">{{ item.title }}</a>
    </div>
    <div class="project-description">
      {{ item.description }}
    </div>
    <div class="project-date">
      <small>{{ item.date | date: "%Y-%m-%d" }}</small>
    </div>
  </article>
  {% endfor %}
</div>

---

## 🤖 Robotics

{% assign robotics = site.robotics | sort: 'date' | reverse %}
<div class="projects">
  {% for item in robotics limit:3 %}
  <article class="project">
    {% if item.image %}
    <div class="project-image">
      <img src="{{ item.image.path | relative_url }}" alt="{{ item.title }}">
    </div>
    {% endif %}
    <div class="project-title">
      <a href="{{ item.url }}">{{ item.title }}</a>
    </div>
    <div class="project-description">
      {{ item.description }}
    </div>
    <div class="project-date">
      <small>{{ item.date | date: "%Y-%m-%d" }}</small>
    </div>
  </article>
  {% endfor %}
</div>

---

## 🔬 ML & RL

{% assign mlrl = site.ml_rl | sort: 'date' | reverse %}
<div class="projects">
  {% for item in mlrl limit:3 %}
  <article class="project">
    {% if item.image %}
    <div class="project-image">
      <img src="{{ item.image.path | relative_url }}" alt="{{ item.title }}">
    </div>
    {% endif %}
    <div class="project-title">
      <a href="{{ item.url }}">{{ item.title }}</a>
    </div>
    <div class="project-description">
      {{ item.description }}
    </div>
    <div class="project-date">
      <small>{{ item.date | date: "%Y-%m-%d" }}</small>
    </div>
  </article>
  {% endfor %}
</div>