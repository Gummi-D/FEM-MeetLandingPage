## Purpose

These instructions help AI coding agents be immediately productive in this repository. The project is a small, static landing page (Frontend Mentor "Meet" challenge). Focus on non-invasive, explicit edits and preserve the original file structure and asset naming.

## Quick repo snapshot

- Single HTML entry: `index.html` (root). No build system or package.json is present.
- Static assets under `assets/` with subfolders: `desktop/`, `tablet/`, `mobile/`. Example files: `assets/desktop/logo.svg`, `assets/favicon-32x32.png`.
- No obvious CSS or JS files are committed. Styling and scripts may be missing and expected to be added next to `index.html` (e.g., `styles.css`, `script.js`).
- There is no `README.md` in this repository root — ask the maintainer for challenge specs if functionality requirements are unclear.

## Big-picture architecture / intent

- Purpose: a static, responsive landing page intended to support multiple breakpoints using separate image assets for desktop/tablet/mobile.
- Data flow: none (static content only). Any interactivity should be implemented with lightweight vanilla JS and unobtrusive enhancement.
- Service boundaries: keep changes local to HTML/CSS/asset files. Do not introduce backend services or package managers unless requested.

## Project-specific conventions & patterns

- Assets are organized by breakpoint under `assets/{desktop,tablet,mobile}`. When adding or replacing images, keep the same folder structure and filenames where possible.
- Keep `index.html` as the canonical source of content. Avoid moving content into multiple pages unless explicitly required.
- Favor semantic HTML (section, header, main, footer, nav). If adding CSS, place it as a single `styles.css` and link it from the head of `index.html`.
- Accessibility: add `alt` text for each image in `assets/` and ensure interactive elements (links/buttons) have discernible text and focus styles.

## How to run / preview locally

- No build step. Open `index.html` in a browser for quick preview.
- Recommended ways to serve locally (pick one):

  - Using Python (if available):

    ```powershell
    python -m http.server 8000
    ```

  - Use VS Code Live Server extension for an instant preview.

If you need a Node-based static server, request permission before adding dependencies (no package.json currently).

## What AI agents should do first (safe, high-value edits)

1. Add a minimal `styles.css` and link it in `index.html` (non-destructive change). Keep CSS in a top-level `css/` or `styles/` folder.
2. Replace image tags with proper `alt` attributes and prefer responsive <picture> or srcset patterns if adding new markup.
3. Improve semantics: wrap the main content in `<main>`, add `<header>`/`<footer>` where appropriate, and ensure one `<h1>` exists.
4. When implementing interactions (e.g., download button), use progressive enhancement and keep JS tiny and dependency-free.

## Examples from this codebase

- Favicon is linked in `index.html`: `./assets/favicon-32x32.png` — preserve that path when editing the head.
- Logo file example: `assets/desktop/logo.svg` — when adding responsive images, mirror the existing naming (logo.svg) across breakpoint folders.

## Restrictions & guardrails for agents

- Do not introduce new build tools, package.json, or dependencies without explicit instruction from the maintainer.
- Keep PRs small and focused. Each change should include a one-line description of intent and the minimal files changed.
- Avoid changing filenames of existing assets unless updating references in all HTML/CSS files.

## When to ask the human

- If the task requires behavioral requirements or acceptance criteria (for example exact spacing, animations, or required responsive breakpoints), ask for the original challenge `README.md` or design mockups.
- If adding a Node toolchain or CI is suggested, confirm before creating files like `package.json` or GitHub Actions.

---
If anything above is unclear or you'd like the agent to follow a stricter style (naming conventions, CSS architecture like BEM or utility-first), tell me what style to use and I'll update these instructions.
