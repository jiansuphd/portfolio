# 🛠️ Tech Stack

Technical reference for [`index.html`](https://github.com/jiansuphd/portfolio/blob/main/index.html) — the portfolio site.

---

## Frontend

| Tool | Version | Role | CDN URL |
|------|---------|------|---------|
| HTML5 | — | Structure & semantics | — |
| Tailwind CSS | Latest (Play CDN) | Utility-first styling | `https://cdn.tailwindcss.com` |
| Vanilla JavaScript | ES6+ | Interactions & animations | — |
| Font Awesome | 6.0.0 | Icons | `cdnjs.cloudflare.com` |
| Google Fonts — Inter | Variable | Body text | `fonts.googleapis.com` |
| Google Fonts — Outfit | 400/600/700 | Headings | `fonts.googleapis.com` |

---

## Custom CSS Patterns

| Pattern | Implementation | Used In |
|---------|---------------|---------|
| Glassmorphism | `backdrop-filter: blur(12px)` + `rgba` bg | Nav, cards, slider |
| Ambient orbs | `position: fixed`, `filter: blur(80px)`, `opacity: 0.15` | Global background |
| CSS gradient mesh | `radial-gradient` + `linear-gradient` layered | Hero section |
| Scroll reveal | `opacity: 0 → 1` + `translateY(20px → 0)` via IntersectionObserver | All sections |
| Skill bar animation | `width: 0 → data-width` on scroll trigger | About section |
| Typewriter | Character-by-character `innerHTML` append/erase loop | Hero headline |

---

## JavaScript Modules (all inline, no build step)

| Module | Function | Lines (approx.) |
|--------|----------|-----------------|
| ScrollSpy | Updates active nav link based on `scrollY` vs section offsets | ~25 |
| Typewriter | Cycles through role phrases with type/erase animation | ~35 |
| Image Comparison Slider | Drag/touch handler for before/after overlay | ~50 |
| Scroll Reveal | Adds `.active` class when `.reveal` elements enter viewport | ~20 |
| Skill Bar Trigger | Animates `width` when skill bars scroll into view | ~10 |

---

## Hosting & Deployment

| Service | Purpose |
|---------|---------|
| GitHub Pages | Static site hosting |
| GitHub Actions | (Optional) CI/CD for future build pipeline |

**Deploy method:** Push to `main` → GitHub Pages serves `index.html` directly from repo root.  
**Live URL:** https://jiansuphd.github.io/portfolio/

---

## Assets

| File | Type | Status | Notes |
|------|------|--------|-------|
| `Resume.pdf` | PDF | ✅ Committed | Linked in hero CTA |
| `hero-bg.jpg` | Image | ❌ Missing | Referenced in CSS but not in repo — see [Work Plan §1.2](Work%20Plan.md#12-hero-background--css-mesh-gradient) |

---

## Planned Additions (from [Work Plan.md](Work%20Plan.md))

| Tool | Purpose | Phase |
|------|---------|-------|
| Formspree | Contact form endpoint (no backend) | Phase 2 |
| CSS conic-gradient mesh | Replace missing `hero-bg.jpg` | Phase 1 |

---

**Backlinks:** [README.md](../README.md) | [Work Plan.md](Work%20Plan.md) | [progress.md](progress.md)
