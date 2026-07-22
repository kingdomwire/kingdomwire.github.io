# KingdomWire — repo guide for Claude sessions

This repo IS the live site: every push to `main` republishes kingdomwire.net (GitHub Pages, ~1 min).

Rules:
1. **All article content must follow `EDITORIAL-STYLE.md` — verbatim, no exceptions.** Read it before writing or editing any article.
2. Static flat site: one HTML file per article at repo root, all CSS inline in each page. Copy an existing article page as the template for new ones (keep masthead, footer, related-stories sidebar, JSON-LD, og tags).
3. When adding an article: create the page + an `og/<slug>.png` social card (1200x630) + an art banner from `art/` (or a new tile via `artgen.py` conventions: ink #0B0B0D bg, lavender #6B4E9B, wire-diagram style) + update `sitemap.xml`, `index.html`, the relevant section page(s), and `archive.html`.
4. Art tiles live in `art/*.svg`; themes: maritime, diplomacy, aviation, markets, finance, housing, tech, health, sports, tourism, security, infrastructure, environment, energy, culture, labor, general.
5. `.github/workflows/fetch-asset.yml` (workflow_dispatch: url, path) downloads any public URL into the repo from GitHub's servers — use it for Canva exports and other assets the sandbox can't reach.
6. Site contact: info@kingdomwire.net. Ops details live in the "Kingdom Wire" Claude project (`claude/site-operations-playbook.md`).
