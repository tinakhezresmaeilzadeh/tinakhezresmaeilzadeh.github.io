# Tina Khezresmaeilzadeh — personal site

Plain HTML/CSS, no build step. GitHub Pages serves the repo root as-is.

## Files
- `index.html` — about, experience, education, selected publications
- `research.html` — research directions (descriptions left empty)
- `publications.html` — full paper list grouped by year
- `projects.html` — project cards
- `projects/*.html` — one page per paper; `projects/_template.html` is the blank copy
- `assets/css/style.css` — all styling; light/dark colors are the two token blocks at the top
- `assets/js/theme.js` — moon/sun toggle (remembers the choice)
- `images/profile.jpg` — profile photo
- `images/projects/` — card thumbnails and teaser figures (`<slug>.png`)

## Add a new paper project
1. Copy `projects/_template.html` to `projects/my-paper.html` and fill in title, venue, authors, links, abstract, BibTeX.
2. Put figures in `images/projects/` and swap the "Teaser figure" box for an `<img>`.
3. In `projects.html`, copy one `<article class="card">` block, point the title link at the new page,
   and list Paper/Code/Dataset buttons in `card-links`. To use an image thumbnail, replace the
   `<span class="mark">` with `<img src="images/projects/<slug>.png" alt="">`.
4. In `publications.html`, add a `<li class="pub">` and a "Project page" button.

## Fill in research descriptions
In `research.html`, write text inside each `<p class="desc"></p>`. Empty ones stay hidden.

## Authors on publications
List authors in `pub-authors` and wrap your name in `<span class="me">`.
