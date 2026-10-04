---
layout: about
title: about
permalink: /

profile:
  align: left
  image: prof_pic.jpg
  image_circular: false # crops the image to make it circular

selected_papers: true # includes a list of papers marked as "selected={true}"
social: false # social icons are in the top bar instead (enable_navbar_social in _config.yml)

announcements:
  enabled: true # includes a list of news items
  scrollable: true # adds a vertical scroll bar if there are more than 3 news items
  limit: 5 # leave blank to include all the news in the `_news` folder

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
    .profile {
      width: 25%;
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
  /* small "* denotes equal contribution" note right under "selected publications" */
  .equal-contribution-note {
    font-size: 0.75rem;
    margin-top: -0.4rem;
  }
  /* tighter news list */
  .news td,
  .news th {
    padding-top: 0.25rem;
    padding-bottom: 0.25rem;
  }
</style>

Hi! I'm Michael, a PhD student in the [Paul G. Allen School of Computer Science & Engineering](https://www.cs.washington.edu/) at the University of Washington, where I'm co-advised by [Yulia Tsvetkov](https://homes.cs.washington.edu/~yuliats/) and [Dan Suciu](https://homes.cs.washington.edu/~suciu/).

My goal is to enable non-technical users to analyze and extract high-quality information from large, complex datasets with minimal effort, using only natural-language descriptions. My current work focuses on LLM-based single- and multi-agent systems, where I study and improve how these systems are deployed and orchestrated in open-ended data environments.

Before UW, I did my undergraduate and master's studies at the [Technical University of Crete](https://www.tuc.gr/en/home) in Greece, where I worked on communication-efficient federated learning with [Antonios Deligiannakis](http://users.softnet.tuc.gr/~adeli/) and Vasilis Samoladas.
