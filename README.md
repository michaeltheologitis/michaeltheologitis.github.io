# michaeltheologitis.github.io

Source for my personal website, built with [Jekyll](https://jekyllrb.com/) and the [al-folio](https://github.com/alshedivat/al-folio) theme (v1.2).

## Run locally

Needs Ruby 3.x (Homebrew `ruby@3.4` here) and ImageMagick.

```bash
export PATH="/opt/homebrew/opt/ruby@3.4/bin:$PATH"
bundle install
bundle exec jekyll serve --livereload
```

Then open http://localhost:4000. Pages reload on save; restart the server after editing `_config.yml`.

## Where things live

| What                            | File                                         |
| ------------------------------- | -------------------------------------------- |
| Name, URL, site-wide settings   | `_config.yml`                                |
| Bio, photo, about-page sections | `_pages/about.md`, `assets/img/prof_pic.jpg` |
| News                            | `_news/`                                     |
| Publications                    | `_bibliography/papers.bib`                   |
| CV                              | `_data/cv.yml`                               |
| Social links                    | `_data/socials.yml`                          |
| Blog posts                      | `_posts/`                                    |
