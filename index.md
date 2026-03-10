---
layout: default
---

<div class="hero">
    <h1>{{ site.data.clinic.name }}</h1>
    <p>{{ site.data.clinic.title }}</p>
</div>

<div class="container">
    <section id="about" class="about-split">
        <div class="about-text">
            <h2>{{ site.data.clinic.about_title }}</h2>
            <p><strong>{{ site.data.clinic.about_highlight }}</strong></p>
            <p>{{ site.data.clinic.about_p1 }}</p>
            <p>{{ site.data.clinic.about_p2 }}</p>
        </div>
      <div class="about-image">
        <img src="{{ site.data.clinic.profile_image }}" 
         class="profile-pic"
         srcset="{{ site.data.clinic.profile_image_mobile }} 600w,
                 {{ site.data.clinic.profile_image }} 1300w"
         sizes="(max-width: 600px) 100vw, 650px"
         alt="חזי באר - פסיכולוג קליני"
         width="651" height="434"
         loading="lazy">
      </div>
    </section>

<section id="expertise">
    <h2>תחומי מומחיות</h2>
    <p class="intro-text">{{ site.data.clinic.expertise_intro }}</p>
    <div class="expertise-grid">
        {% for area in site.data.clinic.expertise %}
        <div class="expertise-card {% if area.name == 'קבלת החלטות' %}hide-mobile{% endif %}">
            <div class="card-icon">{{ area.icon }}</div>
            <h3>{{ area.name }}</h3>
            <p>{{ area.description }}</p>
        </div>
        {% endfor %}
    </div>
</section>