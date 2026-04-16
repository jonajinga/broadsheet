# Broadsheet

**A complete, open-source publication system. Fork it, configure it, publish.**

[![MIT License](https://img.shields.io/badge/license-MIT-blue.svg)](LICENSE)
[![Open Collective](https://img.shields.io/opencollective/all/broadsheet?label=backers&color=brightgreen)](https://opencollective.com/broadsheet)
[![Built with Eleventy](https://img.shields.io/badge/built%20with-Eleventy%203-333?logo=eleventy)](https://www.11ty.dev/)

Broadsheet is a production-grade publication platform that builds 500+ pages in under 12 seconds. No database. No framework lock-in. No recurring platform fees. Just Markdown, HTML, CSS, and JavaScript — deployed anywhere static sites run.

It ships with everything a modern publication needs: editorial sections, full-text search, reader tools, dark mode, a public domain library, interactive timelines, events calendar, music player, photo gallery, reviews, games, and 16+ submission forms — all built, tested, and ready to customise.

---

## Why Broadsheet?

Most publishing platforms force a choice: simplicity (but no control) or power (but complexity). Broadsheet gives you both.

| | Broadsheet | Ghost | WordPress | Hugo |
|---|---|---|---|---|
| **Cost** | Free forever | $9-199/mo | Hosting + plugins | Free |
| **Database** | None | MySQL | MySQL | None |
| **Reader tools** | TTS, annotations, highlights, reading list, notes, bookmarks, focus mode, 27 fonts, reading ruler | None | Via plugins | None |
| **Search** | Built-in (Pagefind) | Built-in | Via plugins | Via plugins |
| **Dark mode** | Built-in | Theme-dependent | Via plugins | Theme-dependent |
| **Offline support** | PWA with service worker | No | No | No |
| **CMS** | Pages CMS (free, Git-based) | Built-in | Built-in | Via Netlify CMS etc. |
| **Build time (500 pages)** | ~12 seconds | N/A (server) | N/A (server) | ~5 seconds |
| **Framework** | Vanilla (no React, no build step) | Ember.js | PHP | Go templates |
| **Lock-in** | None (MIT, plain files) | Moderate | Moderate | Low |

---

## Features

### Publishing
- **Configurable editorial sections** with per-section collections, pagination, and RSS feeds
- **Reviews** for books, films, podcasts, and documentaries with ratings
- **Public domain library** with multi-volume works, chapter navigation, floating TOC, reading progress, bookmarks, and annotations
- **Curated collections** — quotes, recommended reading, glossary, timelines, thought experiments, trials
- **Full-screen showcases** — screensaver-style auto-advancing displays for any collection
- **Photo gallery** with lightbox, zoom, download, and category/licence/source filters
- **Video library** for curated embedded content
- **Events calendar** with recurrence engine, month grid, detail panel, and keyboard navigation
- **Music player** — persistent background YouTube player with song collection and playlists
- **Interactive games** — trivia, puzzles, and word games
- **Editions** — group articles into numbered issues, printable as PDF

### Reader Experience
- **27 font choices** (system + Bunny web fonts loaded on demand)
- **Global display settings** — font, size, spacing, theme (light/sepia/cream/dark)
- **Per-page reading settings** — font, size, spacing, width, reading ruler, auto-scroll
- **Text-to-speech** with synced word highlighting (Chrome, Edge)
- **6 highlight colours** with WYSIWYG rich-text note editor
- **Reading ruler** — customisable thickness, colour, and style
- **Focus mode** — dim everything except the article
- **Reading list** — save articles for later
- **Import/export** all reader data as JSON (no accounts needed)
- **Voice search** and form dictation via Web Speech API

### Infrastructure
- **Full-text search** via Pagefind with section filtering, autocomplete, and recent searches
- **Dark mode** with system preference detection and no flash of wrong theme
- **SPA-style navigation** — pages load without full refresh; music and state persist
- **16+ submission forms** via Web3Forms with hCaptcha
- **SEO** — JSON-LD structured data, Open Graph, XML sitemap, per-author RSS
- **Privacy-first analytics** via Umami (cookieless)
- **Comments** via Cusdis
- **Translation** via GTranslate (9 languages)
- **Newsletter** via Buttondown (no open/click tracking)
- **Progressive Web App** with offline support and service worker
- **Print CSS** for articles and editions
- **A-Z glossary** with Tippy.js hover tooltips across all articles
- **Pages CMS** ready — manage all content from a browser without touching code

---

## Quick Start

```bash
git clone https://github.com/jonajinga/broadsheet.git my-publication
cd my-publication
npm install
npm start
```

Open `http://localhost:8080`. The entire site builds in seconds.

---

## Configuration

### Site identity

Edit `src/_data/site.json`:

```json
{
  "title": "Your Publication Name",
  "shortTitle": "YPN",
  "description": "Your tagline here.",
  "url": "https://yoursite.com",
  "email": "hello@yoursite.com",
  "founded": 2026
}
```

This single file controls your publication name, URL, email, navigation, section definitions, analytics, newsletter, comments, and feature flags. Change the values and the entire site updates.

### Visual design

Edit `src/assets/css/tokens.css`:

```css
:root {
  --color-bg:       #F4F1EB;   /* Background */
  --color-ink:      #1A1A1A;   /* Text */
  --color-accent:   #C0392B;   /* Brand accent */
  --color-link:     #2C5F8A;   /* Links */
  --font-masthead:  'Playfair Display', Georgia, serif;
  --font-headline:  'Lora', Georgia, serif;
  --font-body:      'Source Serif 4', Georgia, serif;
  --font-ui:        'DM Sans', system-ui, sans-serif;
}
```

Swap the colours and fonts. Dark mode tokens update automatically.

### Content

Add articles as Markdown files in `src/content/{section}/`:

```yaml
---
layout: article
title: "Your Article Title"
description: "A one-sentence summary."
section: News
author: your-slug
date: 2026-01-15
tags:
  - politics
  - investigation
---

Your article content in Markdown...
```

---

## Content Management

Broadsheet works with [Pages CMS](https://pagescms.org/) — a free, Git-based CMS that gives editors a browser UI for creating and editing content without touching code.

1. Sign in at [app.pagescms.org](https://app.pagescms.org) with your GitHub account
2. Connect your Broadsheet repository
3. Edit articles, quotes, events, glossary terms, and all other content through structured forms

The `.pages.yml` configuration file defines fields for every content type.

---

## Deployment

### Cloudflare Pages (recommended)
1. Push to GitHub
2. Connect in Cloudflare Pages dashboard
3. Build command: `npm run build`
4. Output directory: `_site`
5. Environment variable: `NODE_VERSION = 18`

### Netlify
Build command: `npm run build` | Output: `_site`

### Vercel
Build command: `npm run build` | Output: `_site`

### Self-hosted
Run `npm run build` and serve the `_site` directory with any static file server.

---

## Project Structure

```
src/
├── _data/            # Site config, authors, quotes, events, timeline, etc.
├── _includes/
│   ├── layouts/      # base, article, section, library-chapter, glossary-entry
│   └── partials/     # header, footer, article-card, subscribe, etc.
├── assets/
│   ├── css/          # tokens, base, layout, components, article, library
│   └── js/           # search, annotations, TTS, music player, SPA nav, etc.
├── content/          # Articles by section (news, opinion, analysis, etc.)
├── library/          # Public domain works with chapters
├── glossary/         # A-Z glossary terms (Markdown)
├── bookshelf/        # Recommended reading (Markdown)
├── thought-experiments/
├── trials/
├── music/            # Music page (songs + playlists)
├── games/            # Interactive games
├── pages/            # Static pages (about, privacy, contact, etc.)
└── index.njk         # Home page
```

---

## Contributing

We welcome contributions of all kinds. See [CONTRIBUTING.md](CONTRIBUTING.md) for guidelines.

---

## Roadmap

See [ROADMAP.md](ROADMAP.md) for planned features and long-term vision.

---

## Support the Project

Broadsheet is built and maintained by a solo developer. If you find it useful, please consider supporting its development:

- [Open Collective](https://opencollective.com/broadsheet) — recurring or one-time contributions
- [GitHub Sponsors](https://github.com/sponsors/jonajinga)
- Star the repo and share it with others

Every contribution helps keep the project independent and actively maintained.

### Backers

[![Backers](https://opencollective.com/broadsheet/backers.svg?width=890)](https://opencollective.com/broadsheet#backers)

### Sponsors

[![Sponsors](https://opencollective.com/broadsheet/sponsors.svg?width=890)](https://opencollective.com/broadsheet#sponsors)

---

## Built with Broadsheet

Using Broadsheet for your publication? [Open an issue](https://github.com/jonajinga/broadsheet/issues/new?title=Built+with+Broadsheet&body=Publication+name+and+URL) and we will add you here.

- [The Freethinking Times](https://thefreethinkingtimes.com) — Independent freethought journalism

---

## License

[MIT](LICENSE) — use it for anything. No attribution required, though appreciated.

Built by [Jon Ajinga](https://github.com/jonajinga). Maintained by [Pikes Peak Web Designs](https://www.pikespeakwebdesigns.com).
