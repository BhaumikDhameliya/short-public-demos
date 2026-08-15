# short-public-demos

A small portfolio of standalone, single-page frontend demos — each one built to showcase a real-world integration or client project, deployed live on GitHub Pages.

**Live site:** [scrapiq.in](https://scrapiq.in) ([github.io fallback](https://bhaumikdhameliya.github.io/short-public-demos/))

## What's here

`index.html` at the repo root is the landing page — a dark, animated card grid that links out to each demo. Every demo lives in its own folder and is fully self-contained (no build step, no shared dependencies).

| Demo | Folder | What it shows |
|---|---|---|
| Supabase + Vercel Integration | [`supabase-integration/`](supabase-integration/) | Static HTML site wired to Supabase — form submissions, email capture, live table inserts, and a Zapier automation trigger. |
| TikTok Data Pro — API Playground | [`tiktok-api/`](tiktok-api/) | A RapidAPI product playground: featured creator/hashtag previews matching the real API's response shape, with a subscribe CTA for full access. |
| Pooja Automation — 3D Industrial Site | [`pooja-automation/`](pooja-automation/) | Client site for a shrink-wrap machinery manufacturer — WebGL machine model, scroll-pinned camera, glassmorphic UI, and an inquiry form, built with Three.js, GSAP, and Lenis. |

## Stack

Plain HTML/CSS/JS per demo — no framework, no bundler. Common choices across demos:
- [Tailwind CDN](https://tailwindcss.com) for styling
- [Three.js](https://threejs.org) / [GSAP](https://gsap.com) / [Lenis](https://lenis.darkroom.engineering) where a demo needs 3D or scroll-driven animation
- Direct calls to third-party APIs (Supabase, RapidAPI) — no backend of its own

## Deployment

[`.github/workflows/static.yml`](.github/workflows/static.yml) deploys the entire repo to GitHub Pages on every push to `master`. There's no build step — whatever is in the repo is what's served, live within about a minute of pushing.

## Adding a new demo

```bash
# 1. Create a folder for the new demo
mkdir your-demo-name

# 2. Drop the HTML file in as index.html
mv new_demo.html your-demo-name/index.html

# 3. Add a card for it in the root index.html
#    — copy the commented-out template between
#    "ADD NEW DEMOS BELOW THIS LINE" and "END NEW DEMOS"
#    in index.html, fill it in, and update the numbering.

# 4. Push
git add .
git commit -m "Add: your demo name"
git push origin master

# 5. It's live within ~60 seconds at:
# https://scrapiq.in/your-demo-name/
```
