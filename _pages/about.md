---
layout: about
title: about
permalink: /

profile:
  align: left
  image: prof_pic.jpg
  image_circular: false # crops the image to make it circular

selected_papers: true # includes a list of papers marked as "selected={true}"
social: false # the social icons are under the bio instead (see .bio-socials below)

announcements:
  enabled: true # includes a list of news items
  scrollable: true # adds a vertical scroll bar if there are more than 3 news items
  limit: # blank = all news; the list scrolls (see the style block below)

latest_posts:
  enabled: false
  scrollable: true # adds a vertical scroll bar if there are more than 3 new posts items
  limit: 3 # leave blank to include all the blog posts
---

<style>
  /* al-folio sizes the profile photo at 30% of the page width (full width on phones); make it smaller */
  @media (max-width: 575.98px) {
    .profile {
      width: 60%;
      margin-bottom: 1rem;
    }
    /* on phones, start the bio below the photo instead of squeezing it alongside */
    .profile + .clearfix {
      clear: both;
    }
  }
  @media (min-width: 576px) {
    /* photo (25% wide) and bio side by side; the social icons sit at the bottom of the bio column, just above
       the bottom of the photo. When the bio is taller than the photo, the photo centers against the text and
       icons instead of hugging the top (lifted a few pixels, which looked better than exact centering). */
    article {
      display: grid;
      grid-template-columns: calc(25% + 1rem) 1fr;
    }
    article > * {
      grid-column: 1 / -1;
    }
    article > .profile {
      grid-column: 1;
      width: auto;
      align-self: center;
      position: relative;
      top: -4px;
    }
    article > .profile figure {
      margin-bottom: 0;
    }
    article > .profile + .clearfix {
      grid-column: 2;
      display: flex;
      flex-direction: column;
    }
    .bio-socials {
      margin-top: auto;
      margin-bottom: 0.6rem;
    }
    /* keep the old gap above "news" (the photo's figure margin no longer adds to it) */
    article > .clearfix + h2 {
      margin-top: 3rem;
    }
  }
  /* a bit more room above "news" and "selected publications" */
  article > h2 {
    margin-top: 2rem;
  }
  /* same gap between the news and "selected publications" as above "news" */
  article > .news + h2 {
    margin-top: 3rem;
  }
  /* small "* denotes equal contribution" note right under "selected publications" */
  .equal-contribution-note {
    font-size: 0.75rem;
    margin-top: -0.4rem;
    margin-bottom: 1.25rem;
  }
  /* the note's margin above is enough; on the grid layout the two margins would add up */
  article > .publications {
    margin-top: 0;
  }
  /* social icons under the bio */
  .bio-socials {
    line-height: 1;
  }
  .bio-socials a {
    font-size: 1.9rem;
    margin-right: 0.9rem;
    color: var(--global-text-color);
  }
  .bio-socials a:hover {
    color: var(--global-theme-color);
  }
  /* tighter news list */
  .news td,
  .news th {
    padding-top: 0.25rem;
    padding-bottom: 0.25rem;
  }
  /* scrollable news inside a faint rounded border, so it reads as one box while scrolling */
  :root {
    --news-border-color: rgba(0, 0, 0, 0.06);
  }
  html[data-theme="dark"] {
    --news-border-color: rgba(255, 255, 255, 0.08);
  }
  .news {
    border: 1px solid var(--news-border-color);
    border-radius: 0.5rem;
    padding: 0.25rem 0.5rem;
  }
  /* about four items visible, scroll for the rest (overrides al-folio's inline max-height: 60vw, which never
     kicks in on laptops); the items near the bottom fade out until the list is scrolled to the end */
  .news .table-responsive {
    max-height: 9.25rem !important;
    overflow-y: auto;
    -webkit-mask-image: linear-gradient(to bottom, #000 calc(100% - 2.5rem), transparent);
    mask-image: linear-gradient(to bottom, #000 calc(100% - 2.5rem), transparent);
  }
  .news .table-responsive.at-end {
    -webkit-mask-image: none;
    mask-image: none;
  }
  .news table {
    margin-bottom: 0;
  }
  @media (max-width: 575.98px) {
    .news .table-responsive {
      max-height: 15.25rem !important;
    }
  }
</style>

<script>
  // drop the news fade once the list is scrolled to the end (or if it doesn't scroll at all)
  document.addEventListener("DOMContentLoaded", function () {
    document.querySelectorAll(".news .table-responsive").forEach(function (box) {
      function update() {
        box.classList.toggle("at-end", box.scrollTop + box.clientHeight >= box.scrollHeight - 2);
      }
      box.addEventListener("scroll", update, { passive: true });
      window.addEventListener("resize", update);
      update();
    });
  });
</script>

Hi! 👋

I'm a PhD student in Computer Science & Engineering at the [University of Washington](https://www.cs.washington.edu/), co-advised by [Yulia Tsvetkov](https://homes.cs.washington.edu/~yuliats/) and [Dan Suciu](https://homes.cs.washington.edu/~suciu/).

My research interests center around memory: how AI systems represent, organize, and use information to solve long-horizon, data-intensive tasks—from data representation and context management to agent harnesses, meta-harnesses, and ultimately, self-improvement.

More broadly, I care about making it possible for people like journalists, lawyers, and scientists to ask complex questions over large collections of structured and unstructured data, while ensuring that the answers are inspectable, trustworthy, and transparent. I want to make this happen with smaller models that people can run and control locally.

Feel free to reach out at <a href="mailto:{{ 'mthe@cs.washington.edu' | encode_email }}">mthe [at] cs.washington.edu</a> if you are interested in my work!

<div class="bio-socials">{% social_links %}</div>
