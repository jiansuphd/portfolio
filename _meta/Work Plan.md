# 🗺️ Portfolio Design Improvement Work Plan

**File:** [`index.html`](https://github.com/jiansuphd/portfolio/blob/main/index.html)  
**Live Site:** https://jiansuphd.github.io/portfolio/  
**Created:** 2026-05-05  
**Status:** Planning

---

## 🔍 Audit Summary

| Area | Current State | Severity |
|------|--------------|----------|
| Mobile nav | No hamburger menu  -  all links hidden on small screens | 🔴 Critical |
| Hero background | References `hero-bg.jpg` which does not exist in repo | 🔴 Critical |
| Image slider | Uses `via.placeholder.com`  -  broken/unprofessional | 🔴 Critical |
| Skill bars | Percentage bars (`75% HTML`)  -  UX anti-pattern | 🟡 Medium |
| Portfolio filter | No category tabs  -  visitors must scroll all cards | 🟡 Medium |
| Contact | Raw `mailto:` only  -  no form, no friction-free option | 🟡 Medium |
| Testimonial | Placeholder "Jane Doe, Ph.D." visible on live site | 🟡 Medium |
| Accessibility | Missing `aria-label`, slider not keyboard-navigable | 🟡 Medium |
| Performance | Duplicate CSS blocks, no `defer` on scripts | 🟢 Low |
| ADDIE steps | No visual connector between the 5 process cards | 🟢 Low |

---

## 📦 Phase 1  -  Critical Fixes (Ship First)

**Goal:** Eliminate anything broken or embarrassing on the live site.

### 1.1 Mobile Hamburger Menu ✅
- Add a `☰` button visible only on `md:` breakpoint and below
- Clicking opens a full-width slide-down nav panel
- Close on link click or outside tap
- Estimated lines changed: ~40

### 1.2 Hero Background  -  CSS Mesh Gradient ✅
- Remove dependency on missing `hero-bg.jpg`
- Replace with a self-contained CSS `conic-gradient` / `radial-gradient` mesh
- No image file required, renders perfectly on all devices
- Keep the existing dark `#0f172a` base tone

### 1.3 Image Comparison Slider  -  Replace Placeholders ✅
- Replace `via.placeholder.com` URLs with styled CSS panels
- "Before" panel: dark slate with a simple list/text mockup (the "old LMS")
- "After" panel: a cyan/blue card mockup (the "new hub")
- Pure CSS/HTML  -  no external images needed

---

## 📦 Phase 2  -  UX Improvements

**Goal:** Make the page more useful and professional for hiring managers.

### 2.1 Portfolio Filter Tabs ✅
- Add `All | Canvas | Storyline | HTML | Research` button row above the grid
- Filter by `data-category` attribute on each card
- Smooth CSS opacity transition on hide/show
- No library needed  -  ~30 lines of JS

### 2.2 Skill Bars → Tool Icon Grid ✅
- Remove percentage bars (meaningless to non-technical readers)
- Replace with a 3-column icon + label grid: Canvas, Storyline, Figma, HTML/CSS/JS, Agile, Python/AI
- Each tool chip has a color-coded badge and hover tooltip with context
- Cleaner and more honest signal of tooling

### 2.3 Testimonial  -  Fix or Remove Placeholder ✅
- Either replace "Jane Doe, Ph.D." with a real attribution or remove the section
- If keeping, add a subtle "(name withheld)" note for authenticity

### 2.4 Contact Form ✅ (mailto only pending Formspree ID)
- Add a lightweight 3-field form (Name, Email, Message) above the mailto button
- POST to [Formspree](https://formspree.io)  -  free tier, no backend
- Show a success/error inline message after submit
- **Note:** Formspree placeholder removed; mailto CTA active; re-add form when real Formspree ID obtained

---

## 📦 Phase 3  -  Polish & Accessibility

**Goal:** Pass a basic accessibility audit and tighten visual details.

### 3.1 Accessibility Pass
- Add `aria-label` to all icon-only buttons and links
- Make image comparison slider keyboard-navigable (`ArrowLeft`/`ArrowRight` keys)
- Add `aria-current="page"` to active nav link
- Ensure all color contrasts pass WCAG AA (check cyan on white)

### 3.2 ADDIE Process  -  Connector Lines
- Add a subtle horizontal dashed line or arrow connector between the 5 steps on desktop
- On mobile, convert to a vertical stepper with numbered circles

### 3.3 Performance Cleanup
- Remove duplicate `#navbar .nav-link.active` CSS declaration (appears twice)
- Add `defer` attribute to Font Awesome CDN `<link>` preload
- Consolidate all custom CSS into one `<style>` block

### 3.4 Footer  -  Add Nav Links
- Add quick links (Home, Portfolio, About, Contact) to footer
- Prevents dead-end scrolling experience

---

## 🗓️ Execution Order

| Phase | Items | Effort | Priority |
|-------|-------|--------|----------|
| Phase 1 | 1.1 + 1.2 + 1.3 | ~2 hrs | Do first |
| Phase 2 | 2.1 + 2.2 + 2.3 + 2.4 | ~3 hrs | Do second |
| Phase 3 | 3.1 + 3.2 + 3.3 + 3.4 | ~2 hrs | Polish last |

---

## ✅ Checklist


### Phase 1
- [x] 1.1 Mobile hamburger menu
- [x] 1.2 CSS mesh hero background (no image dependency)
- [x] 1.3 Image slider  -  CSS mockup panels

### Phase 2
- [x] 2.1 Portfolio filter tabs
- [x] 2.2 Tool icon grid replaces skill bars
- [x] 2.3 Testimonial  -  real attribution or remove
- [x] 2.4 Contact  -  mailto CTA (Formspree pending real ID)

### Phase 3
- [x] 3.1 Accessibility: aria-labels, keyboard slider, aria-current
- [x] 3.2 ADDIE step connectors
- [x] 3.3 Duplicate CSS removal + defer scripts
- [x] 3.4 Footer quick-links

---

**Backlinks:** [README.md](../README.md) | [progress.md](progress.md)
