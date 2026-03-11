# Ash — A Reflective Quotes Journal

A calm, aesthetic, single-page quotes website built for **Aashi**. Designed to feel like a modern digital journal — emotional, introspective, and beautiful.

---

## Live Site

Deploy the single `index.html` file to [GitHub Pages](https://pages.github.com/) and it works out of the box. No build steps, no dependencies, no server required.

---

## Features

### Quotes
- Quotes are automatically loaded from a **Google Docs** source
- Each line in the document becomes its own quote card
- Quotes **auto-refresh every 3 minutes** without reloading the page
- Graceful error state shown if the fetch fails

### Quote Cards
- Frosted glass card design with soft shadows and shimmer overlays
- Smooth **scroll-reveal animation** as cards enter the viewport (via `IntersectionObserver`)
- Hover lifts the card with a subtle scale and glow effect
- Each card has a **copy button** — copied text is formatted as:

```
"Quote text here."
⁓aashi
```

### ✨ Random Thought Button
- Picks a random quote card, scrolls smoothly to it, and pulses a glow animation around it

### Background & Atmosphere
- Slow animated radial gradient background
- **60 floating particles** that drift gently and react to cursor movement (subtle repulsion effect)
- **Mouse parallax** on the background layer — the gradient shifts slightly as you move your cursor
- **Cursor glow** — a soft radial light follows the mouse (desktop only, hidden on touch devices)

### Theme Switcher
10 hand-crafted colour themes, switchable from the footer. All transitions are smooth:

| Theme | Feel |
|---|---|
| Dark Midnight | Deep charcoal + soft violet — the default |
| Soft Violet | Rich purple tones |
| Soft Lavender | Light lilac background, deep violet text |
| Rose Pink | Dark background with blush/rose accents |
| Midnight Blue | Deep navy with soft sky-blue accents |
| Warm Peach | Cream background with terracotta tones |
| Classic Dark | Near-black with warm gold accents |
| Sage Green | Dark forest tones with soft mint accents |
| Dusty Rose | Warm cream with muted rose tones |
| Aurora | Deep navy with soft teal/aqua accents |

### Footer
- Auto-updating copyright year via JavaScript
- Instagram icon link (opens in new tab) with a theme-aware hover glow

---

## Tech Stack

| Layer | Details |
|---|---|
| HTML | Semantic, single-file |
| CSS | Custom properties, `backdrop-filter`, CSS animations, `IntersectionObserver` |
| JavaScript | Vanilla ES6+, no frameworks or libraries |
| Fonts | Cormorant Garamond (quotes), DM Sans (UI) via Google Fonts |
| Hosting | GitHub Pages (static, zero config) |

---

## File Structure

```
/
└── index.html      — the entire site (HTML + CSS + JS in one file)
└── README.md       — this file
```

---

## How to Deploy on GitHub Pages

1. Create a new GitHub repository
2. Upload `index.html` (and this `README.md`) to the root
3. Go to **Settings → Pages**
4. Set source to `main` branch, `/ (root)`
5. Save — your site will be live at `https://yourusername.github.io/repo-name`

---

## Updating Quotes

Quotes are fetched from a Google Doc. To change them:

1. Open the Google Doc linked in the source
2. Add, edit, or remove lines — each line becomes one quote card
3. Make sure the document is set to **"Anyone with the link can view"**
4. The site will pick up changes automatically on the next refresh cycle (every 3 minutes)

---

## Customisation

| What | Where in `index.html` |
|---|---|
| Quote source URL | `const QUOTES_URL = '...'` near top of `<script>` |
| Refresh interval | `const REFRESH_INTERVAL = 3 * 60 * 1000` |
| Instagram handle | `href` on the `.ig-link` anchor in the footer |
| Add a new theme | Copy any `[data-theme="..."] { }` block in `<style>`, give it a new name, add a button in the footer |
| Number of particles | `const NUM = 60` in the particles IIFE |

---

*Made with care for Aashi — words that stay with you.*
