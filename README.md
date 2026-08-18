# Borhaneddine Hamadou — Personal Portfolio

Static academic portfolio website. Plain HTML + CSS — no frameworks, no build step, no trackers.

## Structure

Multi-page site. Every page shares an identical left sidebar and top nav; the top nav switches pages.

- `index.html` — About + News
- `publications.html` — Publications
- `talks.html` — Talks
- `projects.html` — Projects
- `experience.html` — Teaching + Earlier Industry Experience
- `activities.html` — Awards & Activities
- `contact.html` — Contact
- `css/style.css` — styles (shared by all pages)
- `img/web/` — web-optimized images (auto-resized copies of `img/`)
- `speedboat/` — live demo of the SpeedBoat Industry dashboard (DRIVE® "Float and Serious" hackathon, May 2026), self-contained copy with optimized assets
- `docs/` — CV, papers, PFE report & slides
- `certifications/` — event certificates
- `videos/` — project & award videos
- `robots.txt`, `sitemap.xml`, `favicon.svg` — SEO assets

## Deploy on GitHub Pages

1. Create a repository named **`BorhaneddineHamadou.github.io`** on GitHub.
2. From this folder:
   ```bash
   git init
   git add .
   git commit -m "Portfolio website"
   git branch -M main
   git remote add origin https://github.com/BorhaneddineHamadou/BorhaneddineHamadou.github.io.git
   git push -u origin main
   ```
3. The site goes live at `https://borhaneddinehamadou.github.io/` within a couple of minutes (Settings → Pages if it doesn't auto-enable).
4. Submit the sitemap at [Google Search Console](https://search.google.com/search-console) to speed up indexing.

> Note: the videos are ~50 MB total, which is fine for GitHub Pages (limit is 1 GB per repo, 100 MB per file).

## Updating

- **News**: add a `<li>` at the top of the news list in `index.html`.
- **Publications**: entries are grouped under year headers (`<h3 class="pub-year">`) in `publications.html`. Copy an existing `<article class="pub">` block and edit it.
- **The sidebar / nav is duplicated on every page.** If you change the sidebar or nav, apply the same change to all `*.html` files (or ask Claude to do it once — the pages were generated from a shared template).
- **Photos**: put originals in `img/`, then regenerate optimized copies (max width 1000px, JPEG quality 82) into `img/web/`.
- Keep `sitemap.xml`'s `<lastmod>` date fresh when you make significant changes.
