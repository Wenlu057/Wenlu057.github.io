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
    <div class="fb-embed-wrap">
      <iframe
        class="fb-embed"
        src="https://www.facebook.com/plugins/post.php?href=https%3A%2F%2Fwww.facebook.com%2FSkidmoreCollege%2Fposts%2Fwhat-if-your-commute-could-think-for-itself-azizul-hakim-26-is-using-artificial-%2F1195151842653221%2F&show_text=true&width=560"
        title="Featured student spotlight post from Facebook"
        loading="lazy"
        width="560"
        height="640"
        style="border:none;overflow:hidden"
        scrolling="no"
        frameborder="0"
        allowfullscreen="true"
        allow="autoplay; clipboard-write; encrypted-media; picture-in-picture; web-share">
      </iframe>
    </div>
    <p class="embed-fallback">
      Featured: <a href="https://www.facebook.com/SkidmoreCollege/posts/what-if-your-commute-could-think-for-itself-azizul-hakim-26-is-using-artificial-/1195151842653221/" target="_blank" rel="noopener">Student Spotlight (Facebook)</a>
    </p>
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
