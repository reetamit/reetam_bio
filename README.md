# Reetam Biswas — Personal Portfolio & Biodata

[![Live Site](https://img.shields.io/badge/Live_Site-GitHub_Pages-1a78ba?style=for-the-badge&logo=github)](https://reetamit.github.io/reetam_bio/)
[![Repository](https://img.shields.io/badge/Source_Code-reetam__bio-24292e?style=for-the-badge&logo=github)](https://github.com/reetamit/reetam_bio)

A lightweight, modular personal portfolio website showcasing professional consulting experience, Agentic AI & GitHub Copilot workflows, Machine Learning & Deep Learning projects, achievements, publications, and community memberships.

🔗 **Live Website:** [reetamit.github.io/reetam_bio](https://reetamit.github.io/reetam_bio/)

## Features

* **Modular Section Architecture:** Each portfolio view (`Home`, `Experience`, `Achievements`, `Projects`, `Media`, `Articles`, `Membership`, `Volunteering`) is separated into its own HTML partial inside `sections/` for clean maintenance.
* **Single-Page Tab Navigation:** Instant client-side switching between sections without full-page reloads.
* **Interactive Image Lightbox Modal:** Fullscreen zoom modal for viewing certificates and project visuals using event delegation.
* **Timeline Technical Skills Layout:** Semantic HTML table styled with a continuous vertical timeline accent bar.

## Project Structure

```text
reetam_bio/
├── index.html              # Main shell (navigation bar, section placeholders, modal, footer)
├── style.css               # Global styles, theme colors, timeline skills table, and modal styling
├── images/                 # Profile photo, company logos, project thumbnails, and backgrounds
└── sections/               # Modular HTML partials loaded dynamically via fetch()
    ├── home.html
    ├── experience.html
    ├── achievements.html
    ├── projects.html
    ├── media.html
    ├── articles.html
    ├── membership.html
    └── volunteering.html
```

## Local Development

Because this project uses the JavaScript `fetch()` API to load HTML files from the `sections/` directory, opening `index.html` directly via the `file://` protocol is blocked by browser CORS policies. Serve the project locally using an HTTP server:

### Option 1: Python (Built-in)
```bash
git clone https://github.com/reetamit/reetam_bio.git
cd reetam_bio
python -m http.server 8000
```
Then open `http://localhost:8000` in your browser.

### Option 2: VS Code Live Server
1. Open the `reetam_bio` folder in **VS Code**.
2. Install the **Live Server** extension.
3. Right-click `index.html` and select **Open with Live Server**.

## How to Update Content

* **Edit an Existing Section:** Open the corresponding file inside `sections/` (e.g., `sections/projects.html` or `sections/achievements.html`) and update the HTML directly.
* **Add a New Section:**
  1. Create a new HTML partial in `sections/new-section.html`.
  2. Add a `<div id="new-section" class="page" data-include="sections/new-section.html"></div>` container in `index.html`.
  3. Add a matching link in the `<nav>` bar calling `showPage('new-section')`.

## Deployment

This site is automatically deployed via **GitHub Pages** from the `main` branch of [reetamit/reetam_bio](https://github.com/reetamit/reetam_bio). Any commits pushed to `main` are published directly to [https://reetamit.github.io/reetam_bio/](https://reetamit.github.io/reetam_bio/).

---
*Handcrafted by Reetam Biswas*
