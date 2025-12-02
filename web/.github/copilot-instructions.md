This repository is a minimal static HTML site. Keep suggestions focused, conservative, and directly applicable to the single-file layout.

- Purpose: single-page static site with one root file: `index.html`.
- No build system: there are no npm/webpack/Makefile targets. Do not add heavy toolchains unless the user asks.

What to change
- Prefer small, incremental edits to `index.html` or new files under the repository root.
- If adding assets, follow the simple convention: create an `assets/` (or `css/`, `js/`, `img/`) folder and reference files with relative paths. Example:
  - `<link rel="stylesheet" href="css/styles.css">`
  - `<script src="js/app.js"></script>`

How to preview locally
- Windows: open the file in the default browser with PowerShell: `Start-Process .\index.html`.
- Or use VS Code Live Server extension and press "Go Live" to serve the folder (recommended for rapid CSS/JS reload).

Testing & CI
- There are no test suites or CI configuration in the repo. If a user requests tests, suggest lightweight approaches (e.g., simple HTML validation, small Playwright/puppeteer smoke test) but do not add them unprompted.

Editing guidance for an AI coding agent
- Be conservative: do not introduce package.json, build steps, or large scaffolding without explicit instruction.
- Keep edits minimal: prefer adding small files (CSS/JS) and updating `index.html` to reference them.
- Use relative links; avoid absolute paths or external CDNs unless the user asks.
- Make suggestions as patch proposals (diffs) rather than large rewritten files.

Examples to reference in suggestions
- Root page: `index.html` (single source of truth for site markup and metadata).
- Recommended asset structure (optional): `css/`, `js/`, `img/`, `assets/`.

If this file already exists
- Merge strategy: preserve existing guidance; add repository-specific notes only if they do not contradict existing writer intent. When in doubt, propose changes as a PR and ask the user.

Questions to ask the user when uncertain
- Should I scaffold a small `css/` and `js/` folder and reference them from `index.html`?
- Do you want a local dev server added (e.g., `live-server` or npm scripts)?

Contact
- Ask for missing context (design system, intended host, automation) before introducing workflows beyond static-file editing.
