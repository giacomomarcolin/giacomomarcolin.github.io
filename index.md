---
layout: default
---

{% assign profile_image_path = "/assets/images/profile_45.jpg" %}
{% assign profile_image = site.static_files | where: "path", profile_image_path | first %}

<section class="profile-intro" aria-labelledby="intro-title">
  <div class="profile-intro__copy">
    <h1 id="intro-title">Giacomo Marcolin</h1>
    <p class="intro-bio">I am a PhD student in Economics at Northwestern University. My research interests are in labor economics and public economics. In the 2026&ndash;27 academic year, I will be a <a href="https://www.nber.org/programs-projects/projects-and-centers/gender-economy/gender-economy-fellows">NBER Gender in the Economy dissertation fellow</a>.</p>
    <p class="intro-bio"><strong>I am on the 2026-2027 job market.</strong> My <strong><a href="#research-category-jmp">job market paper</a></strong> studies gender discrimination based on fertility expectations, using a policy experiment to quantify its contribution to gender gaps in labor market outcomes.</p>
    <p class="intro-bio">Before starting my PhD, I received my MSc in Economics from Bocconi University and my BSc in Economics from the University of Padova.</p>
    <p class="intro-bio">For more information, you can find my CV <a href="{{ '/files/cv/giacomo-marcolin-cv.pdf' | relative_url }}">here</a> and contact me at <a href="mailto:gmarcolin@u.northwestern.edu">gmarcolin@u.northwestern.edu</a>.</p>
  </div>

  {% if profile_image %}
    <img class="profile-photo" src="{{ profile_image_path | relative_url }}" alt="Giacomo Marcolin">
  {% else %}
    <div class="profile-photo-placeholder" role="img" aria-label="Placeholder for a future portrait photograph">
      <span>Photograph<br>coming later</span>
    </div>
  {% endif %}
</section>

<section class="home-research" aria-label="Research">
  {% include research-list.html abstracts="collapsed" context="home" %}
</section>
