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
<aside class="card embed-card" aria-labelledby="featured-media-title">
  <h3 id="featured-media-title" class="embed-title">Featured Media · Student Spotlight</h3>

  <a class="media-card" href="https://www.facebook.com/SkidmoreCollege/posts/what-if-your-commute-could-think-for-itself-azizul-hakim-26-is-using-artificial-/1195151842653221/"
     target="_blank" rel="noopener">
    <img class="media-thumb"
         src="/assets/img/featured/student-spotlight-azizul.jpg"
         alt="Skidmore College Student Spotlight post preview"
         loading="lazy">
    <div class="media-meta">
      <div class="media-kicker">Skidmore College · Facebook</div>
      <div class="media-title">Student Spotlight: Azizul Hakim ’26</div>
      <div class="media-desc">A short feature on our work and student research.</div>
      <div class="media-cta">Open post →</div>
    </div>
  </a>
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
