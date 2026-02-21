---
layout: page
title: Students
subtitle: Current students and alumni collaborators
permalink: /students/
description: "Current and alumni students mentored by Wenlu Du, with roles and project topics."
---

<!-- ## Current Students -->

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

  <aside class="card spotlight-panel" aria-labelledby="featured-media-title">
    <h3 id="featured-media-title" class="embed-title">Featured Media · Student Spotlight</h3>

    <div class="spotlight-stack">
      {% for spotlight in site.data.spotlights %}
      <a class="media-card" href="{{ spotlight.url }}" target="_blank" rel="noopener">
        {% if spotlight.image %}
        <img class="media-thumb"
             src="{{ spotlight.image }}"
             alt="{{ spotlight.title }} preview"
             loading="lazy">
        {% endif %}
        <div class="media-meta{% unless spotlight.image %} media-meta-no-image{% endunless %}">
          {% if spotlight.badge %}<span class="media-badge">{{ spotlight.badge }}</span>{% endif %}
          {% if spotlight.source %}<div class="media-kicker">{{ spotlight.source }}</div>{% endif %}
          <div class="media-title">{{ spotlight.title }}</div>
          {% if spotlight.description %}<div class="media-desc">{{ spotlight.description }}</div>{% endif %}
          <div class="media-cta">Open post →</div>
        </div>
      </a>
      {% endfor %}
    </div>
  </aside>
</div>

<!-- ## Alumni -->

{% for student in site.data.students.alumni %}
<!-- <div class="card student-card">
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
</div> -->
{% endfor %}

If you are interested in joining this group, please see [Join My Lab](/join/).
