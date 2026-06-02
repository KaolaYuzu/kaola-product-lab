# Kaola Product Lab

**AI Product Builder Portfolio — Gate 1**

A capability map and portfolio site showcasing AI product work across five islands: document intelligence, audio QA, music rights, distribution tools, and workflow systems.

Live site: [kaola-product-lab.vercel.app](https://kaola-product-lab.vercel.app) *(coming soon)*

---

## What this is

This is Gate 1 of the Kaola Product Lab — a single-page portfolio built as an interactive capability map. Each island on the map represents a real AI product project.

**Five islands:**
1. PhotoCheck Docs — AI Document Reconstruction
2. Audio QA — AI Audio Quality Assurance
3. Proof of Rights — AI Music Rights Documentation
4. Distributor Fit Quiz — AI Music Release Path
5. Skill System — Repeatable AI Workflow

---

## How to run locally

This is a **single self-contained HTML file**. No build step, no server required.

```bash
git clone https://github.com/your-username/kaola-product-lab.git
cd kaola-product-lab
open index.html   # macOS
# or drag index.html into Chrome/Safari
```

**All assets** (images, icons, backgrounds) are embedded as base64 inline. No external local assets needed.

**External dependencies (require internet):**
- Google Fonts: Cinzel, Montserrat, Noto Sans TC
- Live demo links (Vercel-hosted apps)

---

## Features

- EN / 中文 language toggle (full i18n)
- Interactive island map with Quest Drawers
- About Creator, Contact, Core Skills, Project Gallery modals
- Featured Live Demos → horizontal scroll on mobile
- Mobile Gate 2: responsive layout for ≤768px viewports
- Typography system: Cinzel (EN display) / Montserrat (EN UI) / Noto Sans TC (ZH)

---

## Project structure

```
kaola-product-lab/
├── index.html              # Main file — self-contained, all assets inline
├── README.md               # This file
├── .gitignore
└── docs/
    ├── QA.md               # QA record & known issues
    ├── CHANGELOG.md        # Version history
    └── MOBILE_GATE2.md     # Mobile design proposal & decisions
```

---

## Status

| Version | Status |
|---------|--------|
| Gate 1 Desktop | ✅ Complete |
| Gate 1 Mobile  | ✅ Initial implementation |
| Gate 2 (TBD)   | 🔲 Planned |

---

## Tech stack

Pure HTML / CSS / JavaScript — no frameworks, no build tools.
Single file deployment compatible with GitHub Pages, Vercel, Netlify.

---

## Deploy to GitHub Pages

1. Push this repo to GitHub
2. Go to Settings → Pages
3. Set Source to `main` branch, `/ (root)`
4. Your site will be at `https://your-username.github.io/kaola-product-lab/`
