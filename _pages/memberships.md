---
layout: page
title: "Memberships"
permalink: /memberships/
subtitle: "Affiliations with leading global engineering and research societies."
---

<div class="m-grid">
  {% assign items = site.data.memberships %}
  {% for item in items %}
    {% include membership-card.html item=item %}
  {% endfor %}
</div>
