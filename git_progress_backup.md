# Git & Portfolio Progress Log - April 14, 2026

## 🚀 Portfolio Design Overhaul ("Creative Tech")
The `index.html` file has been completely transformed with a modern, high-impact aesthetic:
- **Glassmorphism**: Applied frosted glass effects (`backdrop-blur-md`) to navigation, portfolio cards, and testimonial containers.
- **Ambient Depth**: Introduced subtle, blurred background orbs (mesh gradients) to add visual sophistication without clutter.
- **Modern Typography**: Switched from Open Sans/Roboto Slab to a tech-forward pairing of **Inter** (body) and **Outfit** (headings).
- **Interactive Features**: 
    - Refined the **Image Comparison Slider** for "Before & After" case studies.
    - Updated the **Typewriter Effect** with new professional strings.
    - Added **Scroll-Reveal animations** and glowing hover states for all project cards.
- **Optimized Content**: Updated the "Process" section to highlight the ADDIE + Agile methodology with a cleaner grid layout.

## 🛡️ Security & Privacy Audit
A thorough security review was conducted for the public GitHub repository:
- **Vulnerability Identified**: The `.obsidian/` folder contained an exposed **Google API Key** and an **RSA Private Key**.
- **Mitigation - .gitignore**: Created a robust `.gitignore` file to permanently exclude `.obsidian/`, `.env` files, and OS-specific metadata.
- **Mitigation - Tracking Removal**: Successfully ran `git rm -r --cached .obsidian/` and pushed the update. **Sensitive configuration files are no longer in the public view of the repository.**
- **Conflict Resolution**: Identified that the `obsidian-git` plugin "Auto Backup" was re-uploading these files; forced a secure commit to override this.

## 📝 Documentation Updates
- **README.md**: Rewritten to provide professional project documentation, including technology stacks, core features, and methodology.
- **Live Link**: Added the official portfolio URL: [https://jiansuphd.github.io/portfolio/](https://jiansuphd.github.io/portfolio/)

## ⚠️ Required Next Steps
1. **Rotate API Key**: Immediately **delete and regenerate** your Google API key in AI Studio, as the previous one is compromised.
2. **Obsidian Git Settings**: Disable "Auto Backup" or ensure it is strictly following the new `.gitignore` rules.
3. **Purge History (Optional)**: To completely remove the compromised keys from the Git history, consider deleting and recreating the GitHub repository.

---
*Logged by Gemini CLI*
