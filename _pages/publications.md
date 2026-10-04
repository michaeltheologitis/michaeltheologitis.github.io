---
layout: page
permalink: /publications/
title: publications
description: "* denotes equal contribution"
nav: true
nav_order: 1
---

<style>
  /* keep paper thumbnails mini on phones (al-folio stretches them to full width) */
  @media (max-width: 575.98px) {
    .publications .preview {
      max-width: 45%;
    }
  }
  /* line the paper pictures up with the top of the title text */
  @media (min-width: 576px) {
    .publications .preview {
      margin-top: 0.5rem;
    }
  }
</style>

<div class="publications">

{% bibliography %}

</div>
