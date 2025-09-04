---
layout: page
permalink: /volunteering/
title: Volunteering
description: Global contributions through mentoring, judging, and reviewing.
nav: true
nav_order: 5
---

<div class="volunteering-cards">
  {% for item in site.data.volunteering %}
  <div class="vol-card">
    <div class="vol-logo">
      <img src="{{ item.logo | relative_url }}" alt="{{ item.organization }}">
    </div>
    <div class="vol-details">
      <h3><strong>{{ item.title }}</strong></h3>
      <p class="vol-org"><strong>{{ item.organization }}</strong> ・ {{ item.year }}</p>
      <p class="vol-desc">{{ item.description }}</p>
    </div>
  </div>
  {% endfor %}
</div>