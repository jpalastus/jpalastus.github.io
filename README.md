# jpalastus.github.io — personal website v2

Static personal website built with **Jekyll** (no theme, custom layout), served automatically by
**GitHub Pages** from this repository (`https://jpalastus.github.io`). No build step is needed
locally: just commit and push to `main`; Pages rebuilds the site (~1 min).

> Keep `profile.png` at the repository root — it is used as the logo/avatar/home photo.

## Structure

| Path | What it is | Edit it to… |
| --- | --- | --- |
| `_config.yml` | Site title, description, url, author identity | change global metadata |
| `_data/navigation.yml` | The top navigation menu | add/remove/reorder pages |
| `_data/socials.yml` | Profiles/socials (Contact page + footer icons) | add a profile (name, url, blurb, SVG path) |
| `_data/contact.yml` | Emails and SIMaP postal address | update contact info |
| `_data/metrics.yml` | Citation metrics on the Publications page | refresh numbers + `as_of` date |
| `_data/publications.yml` | The publication list (newest first) | add/edit a paper (year, title, authors, journal, doi, hal, arxiv, note) |
| `_layouts/default.html` | Page skeleton (head, header, footer) | change global page structure |
| `_includes/header.html` | Header + nav rendering | tweak the header |
| `assets/css/style.css` | **All styling — see `:root` at the top** | change fonts/colors site-wide |
| `assets/js/main.js` | Dark-mode toggle + mobile menu | change interactive bits |
| `index.md` | Bio / home page | edit the home content |
| `cv.md`, `areas.md`, `gallery.md`, `opportunities.md`, `contact.md` | Pages | edit content |
| `publications.html` | Publications page (renders `_data/publications.yml`) | change layout of the list |
| `assets/img/gallery/` | Gallery images | add illustration files + `<figure>` in `gallery.md` |

## Changing the color schema and fonts (the easy way)

Open `assets/css/style.css` and edit the variables in the `:root { … }` block at the very top:

- Fonts: `--font-body`, `--font-heading`, `--font-mono`
- Colors: `--color-bg`, `--color-surface`, `--color-text`, `--color-muted`, `--color-primary`, `--color-accent`, `--color-border`

Dark mode has its own overrides in `[data-theme="dark"] { … }` (toggle with the ◐ button in the
header). Two ready-made alternative palettes are included as comments in the same file — copy one
over `:root` to switch. Nothing else needs to change.

## Changing the menu

Edit `_data/navigation.yml` — each entry is `{ title, url }` where `url` is the page output path
(`/` for home, `/cv.html`, `/publications.html`, …).

## Updating publications and metrics

- Add a paper to `_data/publications.yml` (write your own name as `J. P. A. de Mendonça`, it is
  automatically bolded). Verify DOIs at https://doi.org or via OpenAlex/Crossref.
- Refresh `_data/metrics.yml` numbers and the `as_of` date from Google Scholar / OpenAlex.

## Local preview (optional)

```bash
gem install jekyll bundler   # once
jekyll serve                 # then open http://localhost:4000
```
