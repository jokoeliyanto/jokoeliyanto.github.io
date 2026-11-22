---
layout: single
title: 'Data Analyst dengan Python'
permalink: /free-courses/data-analyst-python/
author_profile: true
---

## Materi Pembelajaran

{% assign python_courses = site.free_course | where_exp: "item", "item.path contains 'data-analyst-python'" | sort: 'date' %}

{% if python_courses.size > 0 %}
<div class="course-materials">
  {% for course in python_courses %}
    <div class="material-item">
      <h3>
        <a href="{{ course.url }}">{{ course.title }}</a>
      </h3>
      {% if course.excerpt %}
        <p>{{ course.excerpt }}</p>
      {% endif %}
      <p class="material-meta">
        <i class="fa fa-calendar"></i> {{ course.date | date: "%B %d, %Y" }}
        {% if course.tags %}
          | <i class="fa fa-tags"></i> {{ course.tags | join: ", " }}
        {% endif %}
      </p>
    </div>
  {% endfor %}
</div>
{% else %}
  <p>Materi sedang disiapkan...</p>
{% endif %}
