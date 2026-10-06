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
    /* keep paper thumbnails mini on phones (al-folio stretches them to full width) */
    .publications .preview {
      max-width: 45%;
    }
  }
  @media (min-width: 576px) {
    /* photo (25% wide) and bio side by side; the social icons sit at the bottom of the bio column, just above
       the bottom of the photo (or right after the text, if the bio ever gets taller than the photo) */
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
    /* line the paper pictures up with the top of the title text */
    .publications .preview {
      margin-top: 0.5rem;
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
  /* scrollable news: about four items visible, scroll for the rest
     (overrides al-folio's inline max-height: 60vw, which never kicks in on laptops) */
  .news .table-responsive {
    max-height: 9rem !important;
    overflow-y: auto;
  }
  @media (max-width: 575.98px) {
    .news .table-responsive {
      max-height: 15rem !important;
    }
  }
</style>

Hi! 👋

I'm a PhD student in Computer Science & Engineering at the [University of Washington](https://www.washington.edu/), co-advised by [Yulia Tsvetkov](https://homes.cs.washington.edu/~yuliats/) and [Dan Suciu](https://homes.cs.washington.edu/~suciu/).

My research interests center around enabling models to manage, reuse, and self-organize their accumulating context in long-horizon tasks—from harnesses and meta-harnesses to context engineering and memory.

More broadly, I care about making it possible for people like journalists, lawyers, and scientists to ask complex questions over large collections of structured and unstructured data, while ensuring that the answers are inspectable, trustworthy, and transparent.

Feel free to reach out at <a href="mailto:{{ 'mthe@cs.washington.edu' | encode_email }}">mthe [at] cs.washington.edu</a> if you are interested in my work!

<div class="bio-socials">{% social_links %}</div>
