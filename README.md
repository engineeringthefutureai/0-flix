# 0-FLIX — Zero-Dollar Zero-Streaming

[![Deploy with Vercel](https://vercel.com/button)](https://vercel.com/new)
[![License: MIT](https://img.shields.io/badge/License-MIT-black.svg)](LICENSE)

> **Zero-dollar zero-streaming, available now.**  
> No subscription. No account. No card. No catalogue. The player is already loaded, because there is nothing to load.

---

## Overview

**0-FLIX** is an easy-to-deploy static website pre-configured for instant hosting on [Vercel](https://vercel.com).

- **Zero configuration:** Deploys out of the box as a static site on Vercel.
- **Modular design:** Built with the Modernist design system, featuring clean unbundled HTML, tokens, and components.
- **Social-ready:** Includes custom vector favicon (`favicon.svg`) and Open Graph / Twitter Cards preview image (`og-image.png`).
- **Production-hardened:** `vercel.json` includes security headers (`nosniff`, `SAMEORIGIN`, `strict-origin-when-cross-origin`), clean URLs, and optimized asset caching.

---

## Quick Start (Local Development)

You can run and test the project locally using any of the following methods:

### Option 1: Using Node & `serve` (Recommended)

```bash
# Start a local static server
npx serve .

# Or using npm scripts
npm install
npm run dev
```

Then visit [http://localhost:3000](http://localhost:3000).

### Option 2: Using Python

```bash
python3 -m http.server 3000
```

Then visit [http://localhost:3000](http://localhost:3000).

### Option 3: Open Directly

You can also double-click [index.html](file:///home/kiryl/agy-workspace/0-flix/index.html) in your browser.

---

## Deploying to Vercel

### Method 1: Git Integration (Recommended)

1. Push this repository to GitHub, GitLab, or Bitbucket.
2. Go to your [Vercel Dashboard](https://vercel.com/dashboard) and click **"Add New Project"**.
3. Import your repository.
4. Leave all build settings as default (Framework Preset: **Other**, Build Command: empty, Output Directory: empty).
5. Click **"Deploy"**. Your site will be live on a `*.vercel.app` URL in seconds!

### Method 2: Vercel CLI

Deploy directly from your terminal using the Vercel CLI:

```bash
# Preview deployment
npx vercel

# Production deployment
npx vercel --prod
```

Or using npm scripts:

```bash
npm run deploy       # preview
npm run deploy:prod  # production
```

### Method 3: Vercel Web Dashboard (Drag and Drop)

1. Navigate to [vercel.com/new](https://vercel.com/new).
2. Drag and drop this project folder directly onto the dashboard to deploy.

---

## Project Structure

```text
0-flix/
├── index.html            # Primary static entry point with SEO & Open Graph meta tags
├── support.js            # Component runtime support script
├── _ds/                  # Modernist design system (styles.css, bundle, readme)
├── vercel.json           # Vercel deployment configuration (cleanUrls, headers, rewrites)
├── package.json          # Project metadata and local dev / deploy scripts
├── favicon.svg           # Vector SVG favicon matching the 0-FLIX branding
├── og-image.png          # 1200x630 social preview card for Twitter / LinkedIn / Discord
├── .gitignore            # Excludes node_modules, .vercel, and OS files
└── README.md             # Documentation and deployment guide
```

---

## Vercel Configuration Highlights

- **`cleanUrls: true`**: Automatically cleans `.html` extensions from URLs.
- **Rewrites**: `/0-FLIX` and `/0-FLIX.html` seamlessly resolve to `/index.html`.
- **Security Headers**: Standard security headers are configured across all routes.
- **Caching**: 1-year immutable caching for static media (`favicon.svg`, `og-image.png`).

---

## License

[MIT](LICENSE)
