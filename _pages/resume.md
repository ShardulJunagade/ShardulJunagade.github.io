---
layout: default
title: cv
permalink: /cv/
nav: true
nav_order: 5
cv_pdf: /assets/pdf/resume.pdf
description: To download my CV, click on the PDF button alongside.
---

<!--
  CV PDF viewer. Uses layout: default and hand-writes the gem's CV header markup,
  since al_folio_cv's template has no content hook to put the iframe in.
  Keep the HTML block below free of blank lines, or kramdown misnests the divs.
-->
<div class="post">
  <header class="post-header">
    <h1 class="post-title">
      {{ page.title }}
      <a href="{{ page.cv_pdf | relative_url }}" target="_blank" rel="noopener noreferrer" class="float-right">
        <i class="fa-solid fa-file-pdf"></i>
      </a>
    </h1>
    {% if page.description %}<p class="post-description">{{ page.description }}</p>{% endif %}
  </header>
  <article>
    <iframe src="{{ page.cv_pdf | relative_url }}#view=FitH&amp;navpanes=0" width="100%" style="width: 100%; height: 85vh; min-height: 600px; border: 1px solid #ddd; border-radius: 4px; margin-bottom: 2rem;" allowfullscreen>
      Your browser cannot display embedded PDFs. Use the PDF button above to download my CV.
    </iframe>
  </article>
  <div class="social">
    <div class="contact-icons">{% social_links %}</div>
    <div class="contact-note">{{ site.contact_note }}</div>
  </div>
</div>
