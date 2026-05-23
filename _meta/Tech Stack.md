# 🛠️ Tech Stack

Technical reference for [`index.html`](https://github.com/jiansuphd/portfolio/blob/main/index.html) — the portfolio site.

---

## 🎨 Frontend Dependencies

| Tool | Version | Role | CDN URL |
| :--- | :--- | :--- | :--- |
| **HTML5** | — | Structure & semantics | — |
| **Tailwind CSS** | Latest (Play CDN) | Utility-first styling | `https://cdn.tailwindcss.com` |
| **Vanilla JavaScript** | ES6+ | Interactions & animations | — |
| **Font Awesome** | 6.0.0 | Icons | `cdnjs.cloudflare.com` |
| **Google Fonts (Inter)** | Variable | Body text | `fonts.googleapis.com` |
| **Google Fonts (Outfit)** | 400/600/700 | Headings | `fonts.googleapis.com` |

---

## ✨ Custom CSS Patterns

| Pattern | Implementation | Used In |
| :--- | :--- | :--- |
| **Glassmorphism** | `backdrop-filter: blur(12px)` + `rgba` bg | Nav, cards, slider |
| **Ambient orbs** | `position: fixed`, `filter: blur(80px)`, `opacity: 0.15` | Global background |
| **CSS gradient mesh** | `radial-gradient` + `linear-gradient` layered | Hero section |
| **Scroll reveal** | `opacity: 0 → 1` + `translateY(20px → 0)` via IntersectionObserver | All sections |
| **Skill bar animation** | `width: 0 → data-width` on scroll trigger | About section |
| **Typewriter** | Character-by-character `innerHTML` append/erase loop | Hero headline |

---

## ⚙️ JavaScript Modules (all inline, no build step)

| Module | Function | Lines (approx.) |
| :--- | :--- | :--- |
| **ScrollSpy** | Updates active nav link based on `scrollY` vs section offsets | ~25 |
| **Typewriter** | Cycles through role phrases with type/erase animation | ~35 |
| **Image Comparison Slider** | Drag/touch handler for before/after overlay | ~50 |
| **Scroll Reveal** | Adds `.active` class when `.reveal` elements enter viewport | ~20 |
| **Skill Bar Trigger** | Animates `width` when skill bars scroll into view | ~10 |

---

## 🛠️ Step-by-Step Guide: Phase 1 & 2 Implementation

### What Languages/Skills Do You Need?
- **HTML**: The structure of the page. All content, navigation, and sections are written in HTML.
- **CSS**: The design and layout. All colors, spacing, gradients, and responsive styles are controlled with CSS (including Tailwind utility classes and custom styles).
- **JavaScript**: The interactivity. All dynamic behaviors (menus, sliders, tab filters) are written in plain (vanilla) JavaScript, directly in `<script>` tags in `index.html`.

**If you are a total beginner:**
- You only need to edit one file: `index.html`.
- You do NOT need to install anything. All tools (Tailwind, Font Awesome) are loaded via CDN links at the top of the file.
- You can use any text editor (VS Code, Atom, Notepad++) and view changes by opening `index.html` in your browser.

### Phase 1 — Critical Fixes
1. **Mobile Hamburger Menu**
   - Add a `<button>` with three bars (☰) that only shows on small screens (`md:hidden` in Tailwind).
   - Clicking the button toggles a slide-down mobile nav panel (`#mobile-menu`).
   - Clicking any link or outside the menu closes it.
   - All logic is in a `<script>` block at the bottom of `index.html`.
2. **CSS Mesh Hero Background**
   - Remove any `<img>` for the hero background.
   - Add a `structural-bg` class to the `<header>` and define a multi-layered `radial-gradient` in the `<style>` block.
   - No image files needed—just CSS.
3. **Image Comparison Slider (CSS Panels)**
   - Replace `<img src="via.placeholder.com">` with two `<div>`s:
     - The "after" panel uses a blue/cyan gradient and a list of new features.
     - The "before" panel uses a dark slate background and a list of old limitations.
   - The slider handle is created by JavaScript and lets you drag to compare.

### Phase 2 — UX Improvements
1. **Portfolio Filter Tabs**
   - Add a row of buttons above the portfolio grid: All, Canvas, Storyline, HTML, Research.
   - Each project card gets a `data-category` attribute.
   - JavaScript listens for tab clicks and shows/hides cards by category.
2. **Tool Icon Grid**
   - Remove skill bars.
   - Add a grid of colored "tool chips" (Canvas, Storyline, HTML/CSS/JS, Agile, AI, UDL/WCAG, Figma, ADDIE).
   - Each chip is a `<div>` styled with Tailwind and custom CSS.
3. **Testimonial Section**
   - Remove the placeholder testimonial ("Jane Doe, Ph.D.").
   - If you want a real testimonial, add a new `<section>` with the quote and attribution.
4. **Contact Section**
   - Remove the Formspree form (unless you have a real Formspree ID).
   - Add a prominent mailto button styled with `btn-gradient`.
   - The button opens the user's email client to send you a message.

---

## 🛠️ Step-by-Step Guide: Phase 3 — Polish & Accessibility

This guide walks you through every detail of Phase 3 improvements: accessibility, ADDIE connectors, performance cleanup, and footer quick-links. Each step is beginner-friendly and mapped to the actual code in `index.html`.

### 3.1 Accessibility Improvements
**Goal:** Make the site more usable for everyone, including those using screen readers or keyboard navigation.
1. **Add `aria-label` to icon-only links/buttons:**
   - Find all `<a>` or `<button>` elements that only show an icon (e.g., the scroll chevron, slider handle).
   - Add `aria-label="[describe action]"` (e.g., `aria-label="Scroll to portfolio"`).
2. **Add `aria-current="page"` to active nav link:**
   - In the nav bar, find the link for the current section/page.
   - Add `aria-current="page"` to that `<a>`.
3. **Make the slider keyboard accessible:**
   - In the slider JS, add event listeners for `ArrowLeft` and `ArrowRight` keys when the slider handle is focused.
   - Ensure the slider handle is focusable: add `tabindex="0"` to the slider handle div.
4. **Check color contrast:**
   - Use a tool like [WebAIM Contrast Checker](https://webaim.org/resources/contrastchecker/) to verify all text/background color pairs meet WCAG AA.

### 3.2 ADDIE Step Connectors
**Goal:** Visually connect the 5 ADDIE process cards for better process clarity.
1. **Desktop (horizontal connector):** Wrap the 5 cards in a parent div with `relative` class. Add an absolutely positioned `<div>` behind the cards, styled as a dashed or arrowed horizontal line. Use Tailwind: `absolute left-0 right-0 top-1/2 h-1 border-t-2 border-dashed border-blue-200 z-0`.
2. **Mobile (vertical stepper):** Use Tailwind responsive classes (`lg:hidden`) to show a vertical connector only on small screens. Add a vertical dashed line and numbered circles beside each card.

### 3.3 Performance Cleanup
**Goal:** Make the site faster and easier to maintain.
1. **Remove duplicate CSS:** Search for repeated CSS rules (e.g., `#navbar .nav-link.active`). Keep only one copy.
2. **Defer Font Awesome:** Add `defer` to the Font Awesome `<link>` tag.
3. **Consolidate custom CSS:** Move all custom CSS into a single `<style>` block in the `<head>`.

### 3.4 Footer Quick-Links
**Goal:** Add navigation links to the footer for better UX.
1. **Edit the `<footer>` section:** Add a `<nav>` with links (Home, Portfolio, About, Contact). Use Tailwind classes.
2. **Add `aria-label="Footer quick links"` to the nav.**

---

## Hosting & Deployment

| Service | Purpose |
|---------|---------|
| GitHub Pages | Static site hosting |
| GitHub Actions | (Optional) CI/CD for future build pipeline |

**Deploy method:** Push to `main` → GitHub Pages serves `index.html` directly from repo root.  
**Live URL:** https://jiansuphd.github.io/portfolio/

## Assets

| File | Type | Status | Notes |
|------|------|--------|-------|
| `Resume.pdf` | PDF | ✅ Committed | Linked in hero CTA |
| `hero-bg.jpg` | Image | ❌ Missing | Referenced in CSS but not in repo — see [Work Plan §1.2](Work%20Plan.md#12-hero-background--css-mesh-gradient) |

## Planned Additions (from [Work Plan.md](Work%20Plan.md))

| Tool | Purpose | Phase |
|------|---------|-------|
| Formspree | Contact form endpoint (no backend) | Phase 2 |
| CSS conic-gradient mesh | Replace missing `hero-bg.jpg` | Phase 1 |

---

**Backlinks:** [README.md](../README.md) | [Work Plan.md](Work%20Plan.md) | [progress.md](progress.md)
