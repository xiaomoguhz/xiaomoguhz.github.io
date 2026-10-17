# xiaomoguhz.github.io

Personal academic homepage of Junjie Wang (王俊杰), hosted on GitHub Pages.
Pure static site (no build step), visually inspired by the light version of
[Minimal Light](https://github.com/yaoyao-liu/minimal-light): a compact author
sidebar on the left and content on the right, with a
reverse-chronological "Recent News" timeline. English only.

Live: https://xiaomoguhz.github.io

## Layout

```
index.html       # sidebar + About / News / Experience / Publications / Honors
style.css        # light-only two-column layout, Crimson Pro, blue links, responsive
image/
  avatar.png     # profile photo
```

Social icons use Font Awesome 6 (loaded via CDN); no local assets needed.
Crimson Pro is loaded from Google Fonts, with serif fallbacks and system fonts
for interface labels. The site stays light even when the system prefers dark mode.
GitHub star badges use Shields.io dynamic JSON badges to read `stargazers_count`
from the GitHub repository API, with `cacheSeconds=3600`. Counts update automatically.

## Maintenance

- **Avatar**: use `image/avatar.png`. The circular photo displays at 170px on desktop and 78px beside the name on phones. Square, >=400px recommended.
- **Recent News**: keep the latest four `<p>` items directly inside `<div class="news">` and older items inside `<details class="older-news">`, in reverse order; date format `(Mon Year)`.
- **Publications**: add/remove `<div class="pub">` blocks under each `pubgroup`. Standard images fit within a 190 x 122px bordered area on desktop, preserving their aspect ratio. Venue labels sit on the thumbnails, and titles link to the paper. Each Code link has a linked Shields.io star badge for the same repository. GDeCLIP leads the visual-perception group with an `IEEE TPAMI` badge and `Accepted` label.
- **Navigation**: sidebar links point to the About, Experience, Publications, and Honors section anchors.
- **Experience**: place `Research Intern` on the left and `Supervised by` on the right of the same row, without parentheses. Stack them on phones. Link supervisor names to confirmed personal homepages when available.
- **Google Scholar**: the sidebar `Google Scholar` link uses `href="#"` as a placeholder; replace with the real URL.
- **News dates**: the GDeCLIP acceptance month (October 2026) follows the author's update. Older entries were filled with the usual decision month of each venue; verify against actual notification dates.

## Local preview

```bash
cd xiaomoguhz.github.io
python3 -m http.server 8000
# open http://localhost:8000
```

## Deploy (GitHub Pages)

The user-pages repo is named `xiaomoguhz.github.io`; pushing to `main` triggers
an automatic Pages build, live at https://xiaomoguhz.github.io within a minute or two.
