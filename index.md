---
layout: default
title: "דף הבית"
---

<section class="hero">
    <div class="container">
        <h1>{{ site.data.clinic.homepage_hero_title }}</h1>
    </div>
</section>

<section class="container section-padding">
    <h2>{{ site.data.clinic.homepage_greeting }}</h2>
    <p style="font-size: 1.2rem; color: var(--text-muted); margin-bottom: 20px;">
        <strong>{{ site.data.clinic.title }}</strong>
    </p>
    <div style="font-size: 1.1rem; max-width: 800px;">
        {{ site.data.clinic.homepage_about }}
    </div>
</section>

<section style="background-color: #f0f2f5;">
    <div class="container section-padding">
        <h2>תחומי מומחיות</h2>
        <p>{{ site.data.clinic.expertise_intro }}</p>
        
        <div class="expertise-grid">
          {% for item in site.data.clinic.expertises %}
            <div class="expertise-card">
                <h3>{{ item.title }}</h3>
                <p>{{ item.description }}</p>
            </div>
          {% endfor %}
        </div>
    </div>
</section>