# Broadsheet

A complete, open-source publication template for independent journalism. Built with [Eleventy](https://www.11ty.dev/).

**No frameworks. No bundlers. No CMS required.** Just HTML, CSS, JavaScript, and Markdown.

## Features

- **Editorial sections** with per-section collections, pagination, and RSS feeds
- **Full-text search** via Pagefind with section filtering
- **Dark mode** with system preference detection and no flash
- **Reader tools** — text-to-speech, focus mode, font settings, reading list, highlights, annotations, bookmarks, downloads, print, citations
- **Public domain library** with multi-volume works, chapter navigation, floating TOC, reading progress
- **Quotes page** with save, share, copy, and author filtering
- **Video library** for curated embedded content
- **RSS reader** with build-time feed fetching
- **Notes & highlights page** aggregating reader annotations across the site
- **Import/export** for all reader data (localStorage-based, no accounts)
- **Newsletter integration** via Buttondown
- **Comments** via Cusdis
- **Analytics** via Umami (privacy-first)
- **Translation** via GTranslate
- **Progressive Web App** with offline support
- **SEO** — JSON-LD structured data, Open Graph, sitemaps, per-author RSS
- **Pages CMS** ready for content management without code
- **Print CSS** for articles and editions

## Quick Start

```bash
git clone https://github.com/jonajinga/broadsheet.git my-publication
cd my-publication
npm install
npm start
```

Open `http://localhost:8080` to preview.

## Customization

1. Edit `src/_data/site.json` with your publication name, URL, email, and feature flags
2. Change colors and fonts in `src/assets/css/tokens.css`
3. Add articles in `src/content/{section}/` as Markdown files
4. Deploy to Cloudflare Pages, Netlify, or Vercel

## Stack

- **[Eleventy 3](https://www.11ty.dev/)** — Static site generator
- **Nunjucks** — Templates
- **Markdown** — Content
- **Vanilla CSS** — Custom properties, no frameworks
- **Vanilla JavaScript** — No frameworks, no build step
- **[Bunny Fonts](https://fonts.bunny.net/)** — Privacy-friendly font CDN
- **[Pagefind](https://pagefind.app/)** — Client-side search

## Deploy

### Cloudflare Pages
Build command: `npx @11ty/eleventy`
Output directory: `_site`
Node version: 18

### Netlify / Vercel
Build command: `npm run build`
Output directory: `_site`

## Content Management

Add a `.pages.yml` file to use [Pages CMS](https://pagescms.org/) for browser-based content editing without Git knowledge.

## License

MIT — use it for anything. No attribution required, though appreciated.

---

Built by [Pikes Peak Web Designs](https://www.pikespeakwebdesigns.com). Extracted from [The Freethinking Times](https://thefreethinkingtimes.com).
