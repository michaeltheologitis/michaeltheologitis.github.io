---
layout: page
permalink: /cv/
title: CV
nav: true
nav_order: 5
---

{% assign cv_pdf = site.static_files | where: "path", "/assets/pdf/cv.pdf" | first %}
{% if cv_pdf %}

<div>
  <p>
    <a href="{{ cv_pdf.path | relative_url }}" download>Download PDF <i class="fa-solid fa-file-arrow-down"></i></a>
  </p>
  <embed src="{{ cv_pdf.path | relative_url }}" type="application/pdf" width="100%" height="900px">
</div>
{% else %}
<div>
  <p>A PDF of my CV is coming soon.</p>
</div>
{% endif %}
