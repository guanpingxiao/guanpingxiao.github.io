# AGENTS.md

## Project Overview

Personal academic website of Guanping Xiao (肖冠平), Associate Professor at the College of Computer Science and Technology, Nanjing University of Aeronautics and Astronautics (NUAA). Hosted on GitHub Pages at `guanpingxiao.github.io`.

## Tech Stack

- Pure HTML + CSS, no framework or build tools
- Google Analytics (gtag.js) for tracking
- GitHub Pages for deployment

## Directory Structure

```
├── index.html              # Main page (sidebar + content layout)
├── 404.html                # Custom 404 with 5s redirect to home
├── files/                  # Static assets
│   ├── style.css           # Global styles
│   ├── nav.css             # Sidebar navigation styles
│   ├── *.pdf               # Presentation slides
│   ├── *.jpg/.png/.gif     # Images and logos
│   └── *-students.txt      # Student lists
├── publications/           # PDF files of academic papers
└── data/                   # Research datasets
    ├── bugreports/          # Bug report raw data & crawler info
    ├── linux.xlsx           # Linux fault triggers dataset
    └── linux_rgbugs.xlsx   # Linux regression bugs dataset
```

## Page Sections (index.html)

Bio → News → Publications → Team → Professional Services → Teaching → Tools → Research Grants → Useful Links

Navigation uses smooth scroll via JavaScript click handlers on sidebar links.

## Key Conventions

- Sidebar layout: fixed left panel (256px) with responsive breakpoints at 700px and 500px
- Publication entries link to PDFs in `publications/` and slides in `files/`
- External artifacts link to GitHub repos (e.g., `github.com/pcart-tools/`)
- News entries follow `YYYY/MM` date format in table rows
- No templating system; all content is hand-edited HTML
