---
layout: page
title: Works-Projects
permalink: /works-projects/
description: Works and projects during my undergrad.
nav: true
nav_order: 3
display_categories: [Projects, Papers Replicate, Ekbana Internship Works, FuseMachine Semester Projects, Core ML Scratch, Hackathon Projects]
horizontal: false
---

<!-- pages/works-projects.md -->
<div class="work-project">
{% if site.enable_project_categories and page.display_categories %}
  <!-- Display categorized works/projects -->
  {% for category in page.display_categories %}
  <a id="{{ category }}" href=".#{{ category }}">
    <h2 class="category">{{ category }}</h2>
  </a>
  {% assign categorized_works = site.data.works | where: "category", category %}
  {% assign sorted_works = categorized_works | sort: "importance" %}
  <!-- Generate cards for each work/project -->
  {% if page.horizontal %}
  <div class="container">
    <div class="row row-cols-1 row-cols-md-2">
    {% for work in sorted_works %}
      <div class="col mb-4">
        <div class="card h-100">
          <a href="{{ work.link }}">
            <img src="{{ work.image }}" class="card-img-top" alt="{{ work.title }}">
          </a>
          <div class="card-body">
            <h5 class="card-title">{{ work.title }}</h5>
            <p class="card-text">{{ work.description }}</p> <!-- Added description here -->
          </div>
        </div>
      </div>
    {% endfor %}
    </div>
  </div>
  {% else %}
  <div class="row row-cols-1 row-cols-md-3">
    {% for work in sorted_works %}
      <div class="col mb-4">
        <div class="card h-100">
          <a href="{{ work.link }}">
            <img src="{{ work.image }}" class="card-img-top" alt="{{ work.title }}">
          </a>
          <div class="card-body">
            <h5 class="card-title">{{ work.title }}</h5>
            <p class="card-text">{{ work.description }}</p> <!-- Added description here -->
          </div>
        </div>
      </div>
    {% endfor %}
  </div>
  {% endif %}
  {% endfor %}

{% else %}

<!-- Display works/projects without categories -->

{% assign sorted_works = site.data.works | sort: "importance" %}

  <!-- Generate cards for each work/project -->

{% if page.horizontal %}

  <div class="container">
    <div class="row row-cols-1 row-cols-md-2">
    {% for work in sorted_works %}
      <div class="col mb-4">
        <div class="card h-100">
          <a href="{{ work.link }}">
            <img src="{{ work.image }}" class="card-img-top" alt="{{ work.title }}">
          </a>
          <div class="card-body">
            <h5 class="card-title">{{ work.title }}</h5>
            <p class="card-text">{{ work.description }}</p> <!-- Added description here -->
          </div>
        </div>
      </div>
    {% endfor %}
    </div>
  </div>
  {% else %}
  <div class="row row-cols-1 row-cols-md-3">
    {% for work in sorted_works %}
      <div class="col mb-4">
        <div class="card h-100">
          <a href="{{ work.link }}">
            <img src="{{ work.image }}" class="card-img-top" alt="{{ work.title }}">
          </a>
          <div class="card-body">
            <h5 class="card-title">{{ work.title }}</h5>
            <p class="card-text">{{ work.description }}</p> <!-- Added description here -->
          </div>
        </div>
      </div>
    {% endfor %}
  </div>
  {% endif %}
{% endif %}
</div>
