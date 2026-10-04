# TODO

## Open

- [ ] **CV PDF.** Put an updated PDF of my CV at `assets/pdf/cv.pdf`. The CV page picks it up automatically (download link + in-page viewer); until then it says "coming soon".
  - Don't use the Dropbox PDF as is: it has my phone number and personal email, and it's out of date (only Dan as advisor, old FDA-Opt title, missing ClaimDB, Deep Reasoning and Realize What Matters).

## Before going live

- [ ] Rename the GitHub repo to `michaeltheologitis.github.io` (the current name is GitHub's profile-README repo) and set up Pages deployment.

## Done

- [x] **Publications: a mini picture per paper instead of the venue badge.** Each paper shows a figure from that paper itself (ClaimDB: Table 1 + Figure 2; FDA-Opt: Figure 2 + Algorithm 1; EDBT: Figure 1), via the `preview` field with images in `assets/img/publication_preview/`. Replace a file there to swap a picture.
- [x] **Short venue line.** "NeurIPS 2026", "ACL 2026", "Preprint", ... from the `venue` field in `_bibliography/papers.bib`, shown via `_includes/hook/bib.liquid`.
- [x] **Social links in the top bar** (`enable_navbar_social: true`), and no icons at the bottom of the about page.
- [x] **Homepage: no text around the photo** (no subtitle, no address lines).
- [x] **Equal-contribution asterisks** on Deep Reasoning (Dean Light\*, me\*, Kshitish Ghate\*) and Realize What Matters (me\*, Dean Light\*), with a small "\* denotes equal contribution" note under the publication headings.
- [x] **Plain author lists.** `_data/coauthors.yml` is empty, so only my name stands out.
- [x] **CV page:** removed all the generated content; it's just the PDF now (see Open).
- [x] **Fun tab icon:** 🐙
- [x] **No "Type to filter" box** on the publications page. (The ⌘K search in the top bar was removed, then brought back.)
- [x] **News: short and light.** No "Launched this website", more room above the headings, tighter items, short lines with an emoji.
