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

## 🛠️ Step-by-Step Guide: Phase 1 & 2 Implementation

### What Languages/Skills Do You Need?
- **HTML**: The structure of the page. All content, navigation, and sections are written in HTML.
- **CSS**: The design and layout. All colors, spacing, gradients, and responsive styles are controlled with CSS (including Tailwind utility classes and custom styles).
- **JavaScript**: The interactivity. All dynamic behaviors (menus, sliders, tab filters) are written in plain (vanilla) JavaScript, directly in `<script>` tags in `index.html`.

**If you are a total beginner:**
- You only need to edit one file: `index.html`.
- You do NOT need to install anything. All tools (Tailwind, Font Awesome) are loaded via CDN links at the top of the file.
- You can use any text editor (VS Code, Atom, Notepad++) and view changes by opening `index.html` in your browser.

---

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

---

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

**To edit or extend any of these features:**
- Find the relevant section in `index.html` (use search/find in your editor).
- Update the HTML for structure, the `<style>` block for design, and the `<script>` block for interactivity.
- Save and refresh your browser to see changes.

**You do NOT need to know React, Node.js, or any build tools.**

---

## 🛠️ Step-by-Step Guide: Phase 3 — Polish & Accessibility

This guide walks you through every detail of Phase 3 improvements: accessibility, ADDIE connectors, performance cleanup, and footer quick-links. Each step is beginner-friendly and mapped to the actual code in `index.html`.

### 3.1 Accessibility Improvements

**Goal:** Make the site more usable for everyone, including those using screen readers or keyboard navigation.

**Steps:**
1. **Add `aria-label` to icon-only links/buttons:**
   - Find all `<a>` or `<button>` elements that only show an icon (e.g., the scroll chevron, slider handle).
   - Add `aria-label="[describe action]"` (e.g., `aria-label="Scroll to portfolio"`).
   - Example: `<a ... aria-label="Scroll to portfolio">`.
2. **Add `aria-current="page"` to active nav link:**
   - In the nav bar, find the link for the current section/page.
   - Add `aria-current="page"` to that `<a>`.
   - Example: `<a ... aria-current="page">Home</a>`.
3. **Make the slider keyboard accessible:**
   - In the slider JS, add event listeners for `ArrowLeft` and `ArrowRight` keys when the slider handle is focused.
   - Move the slider left/right by a set number of pixels on key press.
   - Ensure the slider handle is focusable: add `tabindex="0"` to the slider handle div.
   - Example: `slider.setAttribute('tabindex', '0');`
4. **Check color contrast:**
   - Use a tool like [WebAIM Contrast Checker](https://webaim.org/resources/contrastchecker/) to verify all text/background color pairs meet WCAG AA.
   - Adjust Tailwind classes or custom CSS if needed.

### 3.2 ADDIE Step Connectors

**Goal:** Visually connect the 5 ADDIE process cards for better process clarity.

**Steps:**
1. **Desktop (horizontal connector):**
   - In the ADDIE section, wrap the 5 cards in a parent div with `relative` class.
   - Add a new absolutely positioned `<div>` behind the cards, styled as a dashed or arrowed horizontal line.
   - Use Tailwind: `absolute left-0 right-0 top-1/2 h-1 border-t-2 border-dashed border-blue-200 z-0`.
   - Adjust z-index so the line appears behind the cards.
2. **Mobile (vertical stepper):**
   - Use Tailwind responsive classes (`lg:hidden`) to show a vertical connector only on small screens.
   - Add a vertical dashed line and numbered circles beside each card.
   - Example: `<div class="absolute left-4 top-0 h-full w-1 border-l-2 border-dashed border-blue-200"></div>`
   - Add a small circle for each step, positioned with `top-[%]` or flex/grid utilities.

### 3.3 Performance Cleanup

**Goal:** Make the site faster and easier to maintain.

**Steps:**
1. **Remove duplicate CSS:**
   - Search for repeated CSS rules (e.g., `#navbar .nav-link.active`).
   - Keep only one copy in the `<style>` block.
2. **Defer Font Awesome:**
   - In the `<head>`, add `defer` to the Font Awesome `<link>` tag: `<link ... defer>`.
   - This lets the page render faster before icons load.
3. **Consolidate custom CSS:**
   - Move all custom CSS into a single `<style>` block in the `<head>`.
   - Remove any stray `<style>` tags elsewhere in the file.

### 3.4 Footer Quick-Links

**Goal:** Add navigation links to the footer for better UX.

**Steps:**
1. **Edit the `<footer>` section:**
   - Add a `<nav>` with links: Home, Portfolio, About, Contact.
   - Use Tailwind classes for spacing and hover effects.
   - Example:
     ```html
     <nav class="flex gap-6 ...">
       <a href="#">Home</a>
       <a href="#portfolio">Portfolio</a>
       <a href="#about">About</a>
       <a href="#contact">Contact</a>
     </nav>
     ```
2. **Add `aria-label="Footer quick links"` to the nav for accessibility.**

---

**Tip:** For every change, save `index.html` and refresh your browser to check the result. Use browser dev tools (F12) to inspect elements and debug styles or accessibility attributes.
**Backlinks:** [README.md](../README.md) | [Work Plan.md](Work%20Plan.md) | [progress.md](progress.md)

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
