# 📋 Progress Log

> Append-only ops log. Format: `[YYYY-MM-DD] Category | Description`

---

## 📅 2026-05-05

| # | Category | Description |
|---|----------|-------------|
| 1 | `Init` | Created [`00_meta/`](https://github.com/jiansuphd/portfolio/tree/main/00_meta) folder with `logs/` and `skills/` subfolders |
| 2 | `Docs` | Fetched and added [`karpathy_skills.md`](https://github.com/jiansuphd/portfolio/blob/main/00_meta/karpathy_skills.md) from [vibe-id-daily](https://github.com/jiansuphd/vibe-id-daily/blob/main/00_meta/karpathy_skills.md) — Karpathy-inspired Claude Code guidelines: Think Before Coding, Simplicity First, Surgical Changes, Goal-Driven Execution |
| 3 | `Docs` | Fetched and added [`karpathy_llm_wiki.md`](https://github.com/jiansuphd/portfolio/blob/main/00_meta/karpathy_llm_wiki.md) from [vibe-id-daily](https://github.com/jiansuphd/vibe-id-daily/blob/main/00_meta/karpathy_llm_wiki.md) — LLM reference wiki |
| 4 | `Chore` | Removed `00_meta/logs/` subfolder — files stored directly under [`00_meta/`](https://github.com/jiansuphd/portfolio/tree/main/00_meta) instead |
| 5 | `Docs` | Added [`progress.md`](https://github.com/jiansuphd/portfolio/blob/main/00_meta/progress.md) — this ops log |
| 6 | `Format` | Reformatted `progress.md` as dated table with clickable GitHub links |
| 7 | `Docs` | Updated [`README.md`](https://github.com/jiansuphd/portfolio/blob/main/README.md) with shields badges, repo tree, tech table, and `00_meta/` section links |
| 8 | `Plan` | Created [`Work Plan.md`](https://github.com/jiansuphd/portfolio/blob/main/00_meta/Work%20Plan.md) — 3-phase design improvement roadmap for [`index.html`](https://github.com/jiansuphd/portfolio/blob/main/index.html): Phase 1 Critical Fixes (mobile nav, hero bg, image slider), Phase 2 UX (filter tabs, tool grid, contact form), Phase 3 Polish (a11y, ADDIE connectors, perf) |
| 9 | `Docs` | Created [`Tech Stack.md`](https://github.com/jiansuphd/portfolio/blob/main/00_meta/Tech%20Stack.md) — full frontend dependency table, custom CSS patterns, JS module inventory, hosting setup, assets status |
| 10 | `Revert` | User requested README restored to original; moved expanded content into `Tech Stack.md` |
| 11 | `Decision` | Confirmed `00_meta/` naming convention over `_meta/` — numeric prefix is explicit, portable, and scales with sibling folders (e.g. `10_projects`, `20_archive`) |
| 12 | `Docs` | Created [`Tech Stack.md`](https://github.com/jiansuphd/portfolio/blob/main/00_meta/Tech%20Stack.md) — frontend deps, custom CSS patterns, JS module inventory, hosting, assets status, planned additions |
| 13 | `Format` | User requested README format improvement — partially reviewed; interrupted before implementation |
| 14 | `Log` | Synced full session chat history to [`progress.md`](https://github.com/jiansuphd/portfolio/blob/main/00_meta/progress.md) — all 14 actions from this conversation captured |

## 📅 2026-05-05 (Session 2)

| # | Category | Description |
|---|----------|-------------|
| 15 | `Docs` | Created [`MOC.md`](https://github.com/jiansuphd/portfolio/blob/main/00_meta/MOC.md) — central index for all `00_meta/` files with repo tree and file index table |
| 16 | `Chore` | Stripped duplicate sections from [`README.md`](https://github.com/jiansuphd/portfolio/blob/main/README.md) — removed everything appended below `© 2026` line (Repository Structure, Tech Stack table, Key Features, ADDIE table, Project Intelligence, Security, duplicate Contact) |
| 17 | `Move` | Repository Structure → [`MOC.md`](https://github.com/jiansuphd/portfolio/blob/main/00_meta/MOC.md) |
| 18 | `Move` | Tech Stack table + Key Features + ADDIE table → already in [`Tech Stack.md`](https://github.com/jiansuphd/portfolio/blob/main/00_meta/Tech%20Stack.md) |
| 19 | `Move` | Project Intelligence section → [`MOC.md`](https://github.com/jiansuphd/portfolio/blob/main/00_meta/MOC.md) File Index |
| 20 | `Log` | Synced full Session 2 chat history to [`progress.md`](https://github.com/jiansuphd/portfolio/blob/main/00_meta/progress.md) |
| 21 | `Move` | Security section moved from [`README.md`](https://github.com/jiansuphd/portfolio/blob/main/README.md) → [`MOC.md`](https://github.com/jiansuphd/portfolio/blob/main/00_meta/MOC.md) Security Notes block |
| 22 | `Chore` | Final README strip — removed all content below `© 2026` line; README now ends cleanly at Contact section |
| 23 | `Plan` | Reviewed [`Work Plan.md`](https://github.com/jiansuphd/portfolio/blob/main/00_meta/Work%20Plan.md) — confirmed Phase 1 execution order: 1.1 Mobile hamburger menu → 1.2 CSS mesh hero background → 1.3 Replace placeholder images |
| 24 | `Dev` | Starting Phase 1.1 — Mobile hamburger menu: add `☰` toggle button, slide-down mobile nav panel, close on link click or outside tap |
| 25 | `Log` | Synced Session 3 chat history to [`progress.md`](https://github.com/jiansuphd/portfolio/blob/main/00_meta/progress.md) |

## 📅 2026-05-05 (Session 4)

| # | Category | Description |
|---|----------|-------------|
| 26 | `Dev` | Phase 1.1 — Added mobile hamburger menu to [`index.html`](https://github.com/jiansuphd/portfolio/blob/main/index.html): `☰` toggle button, slide-down nav panel, close on link click or outside tap |
| 27 | `Dev` | Phase 1.2 — Replaced missing `hero-bg.jpg` with self-contained CSS `conic-gradient`/`radial-gradient` mesh in [`index.html`](https://github.com/jiansuphd/portfolio/blob/main/index.html) |
| 28 | `Dev` | Phase 1.3 — Replaced `via.placeholder.com` URLs in image comparison slider with styled CSS panels (dark slate "before" / cyan-blue "after") |
| 29 | `Dev` | Phase 2.1 — Added filter tabs HTML (`All \| Canvas LMS \| Storyline \| HTML \| Research`) above portfolio grid with `data-category` attributes on cards, CSS transitions, and JS show/hide logic |
| 30 | `Dev` | Phase 2.2 — Removed percentage skill bars; replaced with 8-item tool chip grid (Canvas, Storyline, HTML/CSS/JS, Agile, AI, UDL/WCAG, Figma, ADDIE) |
| 31 | `Dev` | Phase 2.3 — Removed placeholder testimonial section ("Jane Doe, Ph.D.") from [`index.html`](https://github.com/jiansuphd/portfolio/blob/main/index.html) |
| 32 | `Dev` | Phase 2.4 — Contact section: removed Formspree placeholder form (`xwpkvdzg` ID); restored prominent `btn-gradient` mailto CTA — Formspree to be re-added when real ID obtained |
| 33 | `Log` | Synced Session 4 Phase 2 activity to [`progress.md`](https://github.com/jiansuphd/portfolio/blob/main/00_meta/progress.md) |

## 📅 2026-05-05 (Session 5)

| # | Category | Description |
|---|----------|-------------|
| 34 | `Audit` | Read [`progress.md`](https://github.com/jiansuphd/portfolio/blob/main/00_meta/progress.md) and [`Work Plan.md`](https://github.com/jiansuphd/portfolio/blob/main/00_meta/Work%20Plan.md) — explained all 4 sessions to user |
| 35 | `Audit` | Verified Phase 1 status against live [`index.html`](https://github.com/jiansuphd/portfolio/blob/main/index.html): **1.1 hamburger menu NOT implemented**, **1.2 CSS mesh hero ✅ confirmed**, **1.3 slider still uses `via.placeholder.com`** — NOT done |
| 36 | `Audit` | Verified Phase 2 status: **2.1 filter tabs ✅**, **2.2 tool chip grid ✅**, **2.3 testimonial removed ✅**, **2.4 mailto CTA ✅** — all confirmed in code |
| 37 | `Plan` | Phase 3 research complete — identified exact targets: duplicate `#navbar .nav-link.active` CSS (lines 166+228), missing hamburger JS/HTML, `via.placeholder.com` at lines 554+558, missing `aria-label` on scroll chevron + slider handle, no `aria-current` on nav, ADDIE grid needs connector, footer needs quick-links |
| 38 | `Log` | Synced Session 5 activity to [`progress.md`](https://github.com/jiansuphd/portfolio/blob/main/00_meta/progress.md) |
