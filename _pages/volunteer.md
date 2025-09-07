---
layout: page
permalink: /volunteering/
title: Volunteering
description: <strong>  Empowering Innovation Worldwide Through Mentoring, Judging, and Speaking. </strong>
nav: true
nav_order: 5
---

<p style="max-width: 720px; margin: 2rem auto 1rem; text-align: center;">
Over the years, I’ve had the privilege of contributing to the global tech ecosystem through mentorship, judging, public speaking, and technical program leadership. As a mentor on platforms like <strong>ADPList</strong>, I offer one-on-one guidance to professionals and students navigating career transitions and engineering challenges. I actively serve as a judge for global competitions and awards, and as a <strong>Technical Program Committee (TPC)</strong> reviewer for prestigious conferences under <strong>IEEE</strong>, <strong>Springer</strong>, and other international research bodies — helping shape the future of innovation, one review at a time.
</p>

<div style="margin-top: 3rem;"></div>
<hr style="margin: 3rem auto; max-width: 700px; border: none; border-top: 1px solid #eee;" />

<!-- ADPList Mentorship Section -->
<div style="text-align: center; margin-top: 2rem;">
  <h2 style="font-size: 2rem; margin-bottom: 0.5rem;">ADPList Mentorship</h2>
  <p style="text-align: center; margin-top: 2rem;">
    Mentorship isn’t just guidance — it’s about unlocking someone’s potential. Through ADPList, I aim to empower mentees with insights, career direction, and the confidence to succeed in tech and beyond.
  </p>
</div>

<div style="margin: 2rem auto; border-radius: 16px; overflow: hidden; box-shadow: 0 4px 14px rgba(0,0,0,0.1); max-width: 750px;">
  <iframe
    src="https://adplist.org/widgets/single-session?src=karan-kumar-ratra&amp;session=42837-mentorship-session"
    width="100%"
    height="500"
    frameborder="0"
    scrolling="no"
    style="border: none;"
  ></iframe>
</div>

<div style="text-align: center; margin-top: 3rem; margin-bottom: 1rem;">
  <h3 style="font-size: 1.5rem; margin-bottom: 0.5rem;">What Mentees Are Saying</h3>
</div>

<div style="margin: 0 auto 3rem auto; padding: 16px; height: 500px; box-shadow: 0 4px 14px rgba(0,0,0,0.1); border-radius: 16px; overflow: hidden; width: 100%; max-width: 750px;">
  <iframe
    src="https://adplist.org/widgets/reviews?src=karan-kumar-ratra"
    title="All Reviews"
    width="100%"
    height="500"
    loading="lazy"
    style="border: 0px;"
  ></iframe>
</div>


<!-- <section style="padding: 1rem; width: 100%; max-width: 380px; min-height: 350px;"><img alt="Impact swag image" class="" src="https://adplist-users-production.s3.us-east-1.amazonaws.com/7f06af6015891aca2b4ca3b646ee1ae6/swags/2296d865-e66b-5a90-9d3f-bfe96a6a2101.webp" height="100%" width="100%" style="background-color: rgb(225, 49, 108); border-radius: 14px;"></section> -->

<div style="margin-top: 3rem;"></div>
<hr style="margin: 3rem auto; max-width: 700px; border: none; border-top: 1px solid #eee;" />

<div style="text-align: center; margin-top: 2rem;">
  <h2 style="font-size: 2rem; margin-bottom: 0.5rem;"> My Volunteering Work </h2>
</div>

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

      <a href="#" class="more-details-link" data-modal="modal-{{ forloop.index }}">Click here for more details</a>
    </div>
  </div>

  <!-- Modal -->
  <!-- Modal -->
<div class="modal" id="modal-{{ forloop.index }}">
  <div class="modal-content">
    <span class="close-button" data-modal="modal-{{ forloop.index }}">&times;</span>
    
    <div class="modal-header">
      {% if item.modal_image %}
              <img src="{{ item.modal_image | relative_url }}" alt="{{ item.organization }} Image" class="modal-logo">
        {% elsif item.logo %}
            <img src="{{ item.logo | relative_url }}" alt="{{ item.organization }} Logo" class="modal-logo">
        {% endif %}

      <div class="modal-text">
        <h2>{{ item.title }} – {{ item.organization }}</h2>
        <p><strong>Year:</strong> {{ item.year }}</p>
      </div>
    </div>

    <p>{{ item.details }}</p>

    {% if item.download_link %}
      <p><a href="{{ item.download_link | relative_url }}" target="_blank" class="vol-link">Download Certificate</a></p>
    {% endif %}

    {% if item.certificate %}
      <img src="{{ item.certificate | relative_url }}" alt="Certificate" class="modal-cert-img">
    {% endif %}

    {% if item.gallery %}
     <div class="modal-gallery">
            {% for image in item.gallery %}
                <a href="{{ image | relative_url }}" data-lightbox="gallery-{{ forloop.parentloop.index }}" data-title="{{ item.title }}">
                <img src="{{ image | relative_url }}" class="modal-gallery-img" alt="Gallery image {{ forloop.index }}">
                </a>
            {% endfor %}
        </div>

    {% endif %}
  </div>
</div>

  {% endfor %}
</div>
