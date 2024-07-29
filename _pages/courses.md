---
layout: page
title: Courses
permalink: /courses/
description: Additional courses that provided me with a strong foundational base and enriched my knowledge significantly
nav: true
nav_order: 8
display_categories: [Deeplearning Specialization, Tensorflow Specialization, Fusemachine, Power Electronics, Renewable Energy Specialization, Data Structure and Algorithms, Introduction to Computer Science, Optimization and Research, Other Courses]
horizontal: false
---

<!-- pages/courses.md -->
<div class="certificates">
{% if site.enable_project_categories and page.display_categories %}
  <!-- Display categorized certificates -->
  {% for category in page.display_categories %}
  <a id="{{ category }}" href=".#{{ category }}">
    <h2 class="category">{{ category }}</h2>
  </a>
  {% assign categorized_certificates = site.data.certificates | where: "category", category %}
  {% assign sorted_certificates = categorized_certificates | sort: "importance" %}
  <!-- Generate cards for each certificate -->
  {% if page.horizontal %}
  <div class="container">
    <div class="row row-cols-1 row-cols-md-2">
    {% for certificate in sorted_certificates %}
      <div class="col mb-4">
        <div class="card h-100">
          <img src="{{ certificate.image }}" class="card-img-top" alt="{{ certificate.title }}">
          <div class="card-body">
            <h5 class="card-title">{{ certificate.title }}</h5>
            <a href="{{ certificate.link }}" class="btn btn-primary">View Certificate</a>
          </div>
        </div>
      </div>
    {% endfor %}
    </div>
  </div>
  {% else %}
  <div class="row row-cols-1 row-cols-md-3">
    {% for certificate in sorted_certificates %}
      <div class="col mb-4">
        <div class="card h-100">
          <img src="{{ certificate.image }}" class="card-img-top" alt="{{ certificate.title }}">
          <div class="card-body">
            <h5 class="card-title">{{ certificate.title }}</h5>
            <a href="{{ certificate.link }}" class="btn btn-primary">View Certificate</a>
          </div>
        </div>
      </div>
    {% endfor %}
  </div>
  {% endif %}
  {% endfor %}

{% else %}

<!-- Display certificates without categories -->

{% assign sorted_certificates = site.data.certificates | sort: "importance" %}

  <!-- Generate cards for each certificate -->

{% if page.horizontal %}

  <div class="container">
    <div class="row row-cols-1 row-cols-md-2">
    {% for certificate in sorted_certificates %}
      <div class="col mb-4">
        <div class="card h-100">
          <img src="{{ certificate.image }}" class="card-img-top" alt="{{ certificate.title }}">
          <div class="card-body">
            <h5 class="card-title">{{ certificate.title }}</h5>
            <a href="{{ certificate.link }}" class="btn btn-primary">View Certificate</a>
          </div>
        </div>
      </div>
    {% endfor %}
    </div>
  </div>
  {% else %}
  <div class="row row-cols-1 row-cols-md-3">
    {% for certificate in sorted_certificates %}
      <div class="col mb-4">
        <div class="card h-100">
          <img src="{{ certificate.image }}" class="card-img-top" alt="{{ certificate.title }}">
          <div class="card-body">
            <h5 class="card-title">{{ certificate.title }}</h5>
            <a href="{{ certificate.link }}" class="btn btn-primary">View Certificate</a>
          </div>
        </div>
      </div>
    {% endfor %}
  </div>
  {% endif %}
{% endif %}
</div>
