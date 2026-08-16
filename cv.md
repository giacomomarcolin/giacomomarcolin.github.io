---
layout: default
title: CV
---

{% assign cv_path = "/files/cv/giacomo-marcolin-cv.pdf" %}
{% assign cv_file = site.static_files | where: "path", cv_path | first %}

# CV

{% if cv_file %}
<p class="cv-download-link"><a href="{{ cv_path | relative_url }}">Download CV</a></p>
{% else %}
<div class="cv-download-placeholder" role="status">
  <span>The CV PDF is not available yet. Add it at <code>{{ cv_path }}</code>.</span>
</div>
{% endif %}
