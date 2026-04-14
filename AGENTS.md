# AGENTS.md

## Project Overview

Personal academic website of Guanping Xiao (肖冠平), Associate Professor at the College of Computer Science and Technology, Nanjing University of Aeronautics and Astronautics (NUAA). Hosted on GitHub Pages at `guanpingxiao.github.io`.

## Tech Stack

- Pure HTML + CSS, no framework or build tools
- Google Analytics (gtag.js) for tracking
- GitHub Pages for deployment

## Directory Structure

```
├── index.html              # Main page (<nav> sidebar + <main> content)
├── 404.html                # Custom 404 page
├── files/
│   ├── style.css           # Global styles (CSS variables, responsive)
│   ├── nav.css             # Sidebar styles (desktop + mobile hamburger)
│   ├── *.pdf               # Presentation slides
│   ├── *.jpg/.png/.gif     # Images and logos
│   └── undergraduate-students.txt
├── publications/           # PDF files of academic papers
└── data/                   # Research datasets
    ├── bugreports/         # Bug report raw data & crawler info
    ├── linux.xlsx          # Linux fault triggers dataset
    └── linux_rgbugs.xlsx   # Linux regression bugs dataset
```

## Page Sections (index.html)

Bio → News → Publications → Team → Professional Services → Teaching → Tools → Research Grants → Useful Links

Sections use `<section id="..." class="section">` with corresponding `<a href="#..." class="nav-link">` in sidebar.

## Key Conventions

### Layout

- Desktop: fixed left sidebar (280px) + scrollable main content with `margin-left: 280px`
- Tablet (≤900px): sidebar becomes top-fixed horizontal bar with hamburger toggle
- Mobile (≤600px): compact top bar, nav links stack vertically on menu open
- CSS variables defined in `:root` for consistent theming

### Sidebar

- `<nav class="sidebar" id="sidebar">` with profile block and `.nav-links` container
- Mobile: `.mobile-header` with `.hamburger` button toggles `.menu-open` on sidebar
- Active link highlighting via `IntersectionObserver` (rootMargin: `-20% 0px -80% 0px`)

### News

- `.news-old` items hidden by default, revealed via `.show-all` on `.news-list`
- Toggle button `#news-toggle` flips between "Show older news" / "Show less"

### Publications

- `.pub-item` uses flex layout: `.pub-venue` (100px fixed) + `.pub-detail` (flex: 1)
- Venues link to journal/conference pages; artifacts link to GitHub repos

### Commit Style

- Format: `Update <filename>` (e.g., `Update index.html`)
- Simple, concise, no description body
- AGENTS.md is not committed; it is a local development reference only
