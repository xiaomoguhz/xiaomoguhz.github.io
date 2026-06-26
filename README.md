# xiaomoguhz.github.io

Personal academic homepage of Junjie Wang (王俊杰), hosted on GitHub Pages.
Pure static site (no build step), in the Size Wu / AcademicPages (Minimal Mistakes)
style: a sticky author sidebar on the left and content on the right, with a
reverse-chronological "Recent News" timeline. English only.

Live: https://xiaomoguhz.github.io

## Layout

```
index.html       # sidebar + About / News / Experience / Publications / Projects / Honors / Education
style.css        # two-column layout, system sans-serif, blue links, responsive
image/
  avatar.svg     # placeholder avatar (initials JW); replace with a real photo
```

Social icons use Font Awesome 6 (loaded via CDN); no local assets needed.

## Maintenance

- **Avatar**: save a photo as `image/avatar.svg` (or `avatar.jpg`, updating the `src` in `index.html`). Square, >=400px recommended.
- **Recent News**: add/remove `<p>` items inside `<div class="news">` in reverse order; date format `(Mon Year)`.
- **Publications**: add/remove `<div class="pub">` blocks under each `pubgroup`.
- **Google Scholar**: the sidebar `Google Scholar` link uses `href="#"` as a placeholder; replace with the real URL.
- **News dates**: currently filled with the usual decision month of each venue; verify against actual notification dates.

## Local preview

```bash
cd xiaomoguhz.github.io
python3 -m http.server 8000
# open http://localhost:8000
```

## Deploy (GitHub Pages)

The user-pages repo is named `xiaomoguhz.github.io`; pushing to `main` triggers
an automatic Pages build, live at https://xiaomoguhz.github.io within a minute or two.
