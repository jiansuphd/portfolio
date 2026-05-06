# 🛠️ Tech Stack

Technical reference for [`index.html`](https://github.com/jiansuphd/portfolio/blob/main/index.html) — the portfolio site.

---

## 🎨 Frontend Dependencies

| Tool | Version | Role | CDN URL |
| :--- | :--- | :--- | :--- |
| **HTML5** | — | Structure & semantics | — |
| **Tailwind CSS** | Latest | Utility-first styling | `https://cdn.tailwindcss.com` |
| **Vanilla JS** | ES6+ | Interactivity & animations | — |
| **Font Awesome** | 6.0.0 | Icon library | `cdnjs.cloudflare.com` |
| **Google Fonts (Inter)** | Variable | Primary body typography | `fonts.googleapis.com` |
| **Google Fonts (Outfit)** | 400/600/700 | Heading typography | `fonts.googleapis.com` |

---

## ✨ Custom CSS Patterns

| Pattern | Implementation Method | Applied In |
| :--- | :--- | :--- |
| **Glassmorphism** | `backdrop-filter: blur(12px)` + `rgba` background | Nav, cards, slider |
| **Ambient Orbs** | `position: fixed`, `filter: blur(80px)`, `opacity: 0.15` | Global background |
| **Gradient Mesh** | `radial-gradient` + `linear-gradient` layering | Hero section |
| **Scroll Reveal** | `opacity: 0 → 1`, `translateY(20px → 0)` | All sections |
| **Skill Animation** | `width: 0 → data-width` on scroll trigger | About section |
| **Typewriter** | Dynamic `innerHTML` cycling loop | Hero headline |

---

## ⚙️ JavaScript Module Inventory

| Module | Purpose | Complexity |
| :--- | :--- | :--- |
| **ScrollSpy** | Nav link active-state synchronization | ~25 lines |
| **Typewriter** | Animated hero headline phrases | ~35 lines |
| **Image Slider** | Before/after touch-drag comparison | ~50 lines |
| **Scroll Reveal** | IntersectionObserver entry animations | ~20 lines |
| **Skill Trigger** | Scroll-activated width animation | ~10 lines |

---

## 🚀 Implementation Guide

### Phase 1 — Critical Fixes
1. **Mobile Menu**: Toggleable slide-down `#mobile-menu` using Tailwind `md:hidden`.
2. **Hero Background**: Multi-layered `radial-gradient` in `<style>` (replaces image).
3. **Comparison Slider**: Two `<div>` panels (Before/After) controlled by JS.

### Phase 2 — UX Improvements
1. **Filter Tabs**: Category-based show/hide for portfolio projects using `data-category`.
2. **Tool Grid**: Replacing skill bars with stylized tool chips.
3. **Contact**: Replace form with mailto `btn-gradient`.

### Phase 3 — Polish & Accessibility
1. **A11y**: Add `aria-label` and `aria-current` attributes.
2. **Connectors**: ADDIE process cards visually linked with dashed lines.
3. **Performance**: Defer Font Awesome, consolidate custom CSS, and prune duplicates.
4. **Footer**: Navigation quick-links added.

---

## 🌐 Hosting & Deployment

- **Service**: GitHub Pages
- **Deploy**: Push to `main` branch → automated serving.
- **URL**: [https://jiansuphd.github.io/portfolio/](https://jiansuphd.github.io/portfolio/)

---

## 📦 Assets & Status

| File | Type | Status | Notes |
| :--- | :--- | :--- | :--- |
| `Resume.pdf` | PDF | ✅ Committed | Linked in hero CTA |
| `hero-bg.jpg` | Image | ❌ Missing | Removed in favor of CSS gradient |
