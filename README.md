# xiaomoguhz.github.io

Personal academic homepage of Junjie Wang (王俊杰), hosted on GitHub Pages.
Pure static site (no build step), in the Size Wu / AcademicPages (Minimal Mistakes)
style: a sticky author sidebar on the left and content on the right, with a
reverse-chronological "Recent News" timeline. English only.

Live: https://xiaomoguhz.github.io

## Layout

```
index.html       # sidebar + About / News / Experience / Publications / Honors
style.css        # two-column layout, Inter, muted blue links, responsive
image/
  avatar.png     # profile photo
```

Social icons use Font Awesome 6 (loaded via CDN); no local assets needed.
Inter is loaded from Google Fonts, with system fonts for Chinese text.
GitHub star badges use Shields.io and update automatically with service caching.

## Maintenance

- **Avatar**: use `image/avatar.png`. The circular photo displays at 220px on desktop and 160px on mobile. Square, >=400px recommended.
- **Recent News**: keep the latest four `<p>` items directly inside `<div class="news">` and older items inside `<details class="older-news">`, in reverse order; date format `(Mon Year)`.
- **Publications**: add/remove `<div class="pub">` blocks under each `pubgroup`. Images fit within a 240 x 120px bordered area on desktop, preserving their aspect ratio. Each Code link has a linked Shields.io star badge for the same repository.
- **Experience**: list supervisors using `Supervised by` and link names to confirmed personal homepages when available.
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
