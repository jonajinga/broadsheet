# Broadsheet Roadmap

This document outlines the current state and planned direction for Broadsheet. Features are listed roughly in order of priority, though community feedback may shift priorities.

---

## Current (v1.0)

Everything listed on the [README](README.md) is shipped and working:
- Editorial sections with pagination, RSS, and per-author feeds
- Full reader tools suite (annotations, highlights, notes, bookmarks, reading ruler, 27 fonts, focus mode)
- Public domain library with chapter navigation
- Full-text search with autocomplete and section filtering
- Dark mode, SPA navigation, offline support (PWA)
- Events calendar, interactive timelines, curated collections
- Music player, photo gallery, reviews, games
- 16+ submission forms, newsletter, comments, analytics
- Pages CMS integration for browser-based content management
- Deployment on Cloudflare Pages, Netlify, or Vercel

---

## Near-term

### Content & Publishing
- **Multi-author workflows** — editor/reviewer/author roles with draft review pipeline
- **Scheduled publishing** — set a future publish date, auto-deploy on schedule
- **Series support** — link articles into multi-part series with navigation
- **Podcast hosting** — RSS feed generation for podcast episodes

### Reader Experience
- **Membership tiers** — free, supporter, premium content gates (no paywall lock-in)
- **Reading statistics** — time spent, articles read, streaks (all local, no tracking)
- **Annotation sharing** — export highlights as formatted cards for social media
- **Cross-device sync** — optional cloud sync for reader data (encrypted, self-hostable)

### Infrastructure
- **Plugin system** — drop-in features as npm packages (e.g. `broadsheet-plugin-podcast`)
- **Theme marketplace** — community themes with one-command switching
- **Multi-language content** — parallel content trees with language switcher
- **Image optimisation pipeline** — automatic AVIF/WebP generation via eleventy-img
- **E-commerce integration** — sell subscriptions, merchandise, or digital downloads

---

## Medium-term

### Platform
- **Broadsheet Cloud** — managed hosting for non-technical publishers (optional, not required)
- **Visual editor** — block-based page builder for non-code customisation
- **API layer** — headless mode with JSON API for custom frontends
- **Activity pub integration** — federate articles across the Fediverse

### Community
- **Template gallery** — curated starting points for different publication types (magazine, newsletter, academic journal, community newspaper)
- **Contributor dashboard** — track PRs, issues, and community health
- **Documentation site** — dedicated docs site with tutorials, guides, and API reference

---

## Long-term Vision

Broadsheet aims to be the default choice for anyone launching an independent publication — the way WordPress became the default for blogs and Ghost became the default for newsletters. The difference: Broadsheet is truly free (no hosting fees, no platform lock-in, no investor pressure), blazing fast (static output), and gives readers tools that no other platform offers.

The goal is not to replace WordPress or Ghost for everyone — it is to serve the publications that value independence, speed, privacy, and reader experience above all else.

---

## How to Influence the Roadmap

- **Vote on features**: React to [issues labeled `enhancement`](https://github.com/jonajinga/broadsheet/labels/enhancement) to signal demand
- **Propose features**: Open a new issue with a clear use case
- **Fund development**: [Support on Open Collective](https://opencollective.com/broadsheet) to accelerate the roadmap
- **Contribute code**: See [CONTRIBUTING.md](CONTRIBUTING.md)
