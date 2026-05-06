# 🧠 Gemini CLI Skills Index

This document serves as a centralized reference for all globally available Gemini CLI skills.

---

## 🛠️ System & Meta-Skills
*The core engine room for session initialization and skill development.*

- **daily-cli-init**
  - **Description**: System initialization for the Gemini CLI to ensure a consistent environment and persona alignment.
  - **Usage**: Triggered at the start of a session to load the Senior ID Persona and verify vault connectivity.
- **defuddle**
  - **Description**: A reasoning skill designed to unpack complex or underspecified requests into actionable plans.
  - **Usage**: Activate when a task feels ambiguous; it asks targeted questions to refine scope.
- **skill-creator**
  - **Description**: Meta-skill for designing, documenting, and implementing new Gemini CLI skills.
  - **Usage**: Use to extend CLI capabilities. It guides you through creating SKILL.md and supporting scripts.

---

## 📚 Knowledge Management & Documentation
*Tools for maintaining the "LLM to Wiki" architecture and vault integrity.*

- **ingest**
  - **Description**: Ingests new raw source documents into the knowledge base, updating the wiki, index, and log.
  - **Usage**: Activate when adding new articles, papers, or transcripts to extracts key info and update entity pages.
- **query**
  - **Description**: Queries the knowledge base and synthesizes answers from existing wiki pages.
  - **Usage**: Use to ask questions against your synthesized wiki; searches index.md and relevant pages.
- **lint**
  - **Description**: Performs a health-check on the wiki to find orphan pages, contradictions, and stale claims.
  - **Usage**: Run periodically to maintain structural integrity and consistency across the vault.
- **work-notes-formatter**
  - **Description**: Ingests, formats, and reorders work notes/emails into structured chronological timelines.
  - **Usage**: Use when processing email histories to ensure summary-led entries and original record preservation.
- **obsidian-markdown**
  - **Description**: Specialized skill for Obsidian Flavored Markdown (wikilinks, callouts, properties).
  - **Usage**: Ensures notes leverage Obsidian's feature set while maintaining high information density.
- **obsidian-bases**
  - **Description**: Manages the core structural templates and "base" notes for the Lead ID framework.
  - **Usage**: Ensures new course folders or project hubs follow standardized vault architecture.
- **obsidian-daily-journal**
  - **Description**: Automates the creation and maintenance of the 01_Daily log entries.
  - **Usage**: Trigger to log tasks, reflections, and context for the next session.
- **add-daily-pointer**
  - **Description**: Generates and adds new "Daily Pointers" to the Vibe Coding Daily Log.
  - **Usage**: Generates a strategic learning guide based on current vault context.

---

## 🎨 Design, UI & Accessibility
*Professional development tools for high-fidelity, compliant web interfaces.*

- **web-design-engineer**
  - **Description**: Enhances AI-generated web pages by injecting design taste, anti-cliché rules, and a structured design system workflow.
  - **Usage**: Use for any visual, interactive, or front-end deliverable to ensure non-generic, high-quality aesthetics.
- **baseline-ui**
  - **Description**: Enforces UI standards for Tailwind CSS projects, including typography and accessibility.
  - **Usage**: Apply constraints to the current conversation or audit specific files for violations.
- **ui-skills**
  - **Description**: Parent skill coordinating accessibility, metadata, and motion performance audits.
  - **Usage**: Acts as an orchestrator for comprehensive UI refinements.
- **ui-ux-pro-max**
  - **Description**: Advanced design workflow combining cognitive load theory with automated execution.
  - **Usage**: Use for high-stakes projects requiring production-grade web interfaces.
- **frontend-design**
  - **Description**: High-fidelity development skill using React, Tailwind, and modern UI primitives.
  - **Usage**: Build production-grade UI components following Baseline UI standards.
- **fixing-accessibility**
  - **Description**: Specialized audit and remediation skill for WCAG 2.1 and ADA compliance.
  - **Usage**: Identifies contrast issues, ARIA gaps, and keyboard navigation issues in HTML/React.
- **fixing-motion-performance**
  - **Description**: Audits and optimizes animations for 60 FPS and reduced-motion preferences.
  - **Usage**: Optimizes durations and checks for layout thrashing in CSS/JS snippets.
- **fixing-metadata**
  - **Description**: Optimizes SEO, Open Graph, and JSON-LD structured data for learning objects.
  - **Usage**: Generate or fix meta tags and social previews for digital assets.
- **web-artifacts-builder**
  - **Description**: Suite for building multi-component React artifacts (TypeScript, shadcn/ui).
  - **Usage**: Use for complex interactive tools requiring state management and bundling.

---

## 📊 Visualization & Presentation
*Transforming logic and data into visual assets.*

- **excalidraw-diagram**
  - **Description**: Generates and edits Excalidraw-compatible JSON for architectural diagrams.
  - **Usage**: Describe a system/process to receive JSON for direct pasting into Excalidraw.
- **mermaid-visualizer**
  - **Description**: Generates Mermaid.js syntax for flowcharts, sequence, and class diagrams.
  - **Usage**: Describe logic flows to receive Mermaid code for Obsidian or web use.
- **json-canvas**
  - **Description**: Specialized tool for creating and manipulating .canvas files (JSON standard).
  - **Usage**: Programmatically generate node-and-edge maps for knowledge graphs.
- **obsidian-canvas-creator**
  - **Description**: Transforms text content into structured Obsidian Canvas files.
  - **Usage**: Provide an outline/article to generate a valid .canvas JSON file with spatial positioning.
- **pptx**
  - **Description**: Comprehensive skill for reading, editing, and creating PowerPoint (.pptx) files.
  - **Usage**: Mention a "deck" or "presentation" to extract text or generate new slides.
- **nanobanana-ppt-skills**
  - **Description**: Integration with NanoBanana for automated slide generation and visual storytelling.
  - **Usage**: Transform scripts or outlines into structured presentations with visual placeholders.

---

## 🎓 Instructional Design & AI Alignment
*Pedagogical tools for course building and AI resilience.*

- **ai-stress-test**
  - **Description**: Conducts an "AI-able Audit" for course assignments to evaluate vulnerability.
  - **Usage**: Use /stress-test [text] to simulate AI completion and receive redesign strategies.
- **canvas-course-builder**
  - **Description**: Workflow for building accessible course environments within Canvas LMS.
  - **Usage**: Focuses on ADA compliance, responsive layout, and OIT-standardized snippets.
- **humanizer**
  - **Description**: Refines AI-generated text to sound natural and aligned with the Senior ID Persona.
  - **Usage**: Humanize course announcements or assignments for specific pedagogical tones.
- **humanizer-zh**
  - **Description**: Chinese-language humanizer optimized for natural Mandarin pedagogical expression.
  - **Usage**: Same as humanizer, but tuned for Chinese linguistic nuances.

---

## ⚡ Engineering Principles: Karpathy-Inspired Guidelines
*Best practices for coding with LLMs, derived from Andrej Karpathy's methodology.*

### 1. Think Before Coding
- **State assumptions explicitly**: Don't guess; ask if uncertain.
- **Present tradeoffs**: Don't pick interpretations silently.
- **Stop when confused**: Clearly define the bottleneck.

### 2. Simplicity First
- **No extra features**: Stick to the requested scope.
- **No speculative abstractions**: Avoid over-engineering.
- **The test**: If a senior engineer would think it's overcomplicated, simplify.

### 3. Surgical Changes
- **Touch only what is necessary**: No "drive-by" refactoring.
- **Match existing style**: Respect the current codebase's conventions.
- **Cleanup your mess**: Remove only the imports/vars/functions YOUR changes made unused.

### 4. Goal-Driven Execution
- **Define success criteria**: Use tests-first.
- **Loop until verified**: Transform imperative tasks into verifiable goals.

*Read more in the original post regarding Andrej Karpathy's methodology and LLM coding pitfalls.*

---
_Last Index Refresh: May 5, 2026_

**Backlink:** [Home MOC](../root_MOC.md)


