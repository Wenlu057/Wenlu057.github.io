---
layout: page
title: Students
subtitle: Current students and alumni collaborators
permalink: /students/
description: "Current and alumni students mentored by Wenlu Du, with roles and project topics."
---

## Current Students

<div class="students-layout">
  <div class="students-list">
    {% for student in site.data.students.current %}
    <div class="card student-card">
      <h3>{{ student.name }}</h3>
      <p><strong>Role:</strong> {{ student.role }}</p>
      <p><strong>Topic:</strong> {{ student.topic }}</p>
    </div>
    {% endfor %}
  </div>

  <aside class="card spotlight-widget" aria-labelledby="student-spotlights-title">
    <h3 id="student-spotlights-title" class="spotlight-widget-title">Featured Media · Student Spotlight</h3>

    <div class="spotlight-stack">
      {% for spotlight in site.data.spotlights %}
      <article class="spotlight-card">
        {% if spotlight.badge %}
        <p class="spotlight-badge">{{ spotlight.badge }}</p>
        {% endif %}

        {% if spotlight.image %}
        <a class="spotlight-image-link" href="{{ spotlight.url }}" target="_blank" rel="noopener">
          <img class="spotlight-thumb" src="{{ spotlight.image }}" alt="{{ spotlight.title }} preview" loading="lazy">
        </a>
        {% endif %}

        <div class="spotlight-meta">
          {% if spotlight.source %}
          <p class="spotlight-source">{{ spotlight.source }}</p>
          {% endif %}

          <h4 class="spotlight-title">{{ spotlight.title }}</h4>

          {% if spotlight.description %}
          <p class="spotlight-desc">{{ spotlight.description }}</p>
          {% endif %}

          <a class="spotlight-link" href="{{ spotlight.url }}" target="_blank" rel="noopener">Open post →</a>
        </div>
      </article>
      {% endfor %}
    </div>
  </aside>
</div>

## Alumni

{% for student in site.data.students.alumni %}
<div class="card student-card">
  <h3>{{ student.name }}</h3>
  <p><strong>Role:</strong> {{ student.role }}</p>
  <p><strong>Topic:</strong> {{ student.topic }}</p>
  {% if student.links %}
  <div class="link-pills">
    {% for link in student.links %}
      <a class="btn btn-outline" href="{{ link.url }}" target="_blank" rel="noopener">{{ link.label }}</a>
    {% endfor %}
  </div>
  {% endif %}
</div>
{% endfor %}

If you are interested in joining this group, please see [Join My Lab](/join/).
