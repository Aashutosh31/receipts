# Development Log

## 2026-10-03

### Initial site

- Created an independent, dependency-free static website for the Receipts Android app.
- Used the supplied real Android screenshots as product imagery and kept the page responsive and keyboard navigable.
- Added Android v1.0.0 release and source links, privacy and security links, and the verified release checksum.
- Set the canonical page and sitemap URL to `https://aashutosh31.github.io/receipts/`.

### Deployment correction

- Changed stylesheet, script, favicon, and image references from domain-root paths to relative paths. GitHub Pages serves this repository beneath `/receipts/`, so root-relative paths would request files from `https://aashutosh31.github.io/` instead of the project site.

### Repository hygiene and checks

- Added `.gitignore` entries for `.agents/`, `.codex/`, editor state, local environment files, logs, and generated output.
- Searched the tracked website source for API keys, secrets, tokens, passwords, and private-key material; none were found.
- Confirmed the site has no backend code, inline event handlers, dynamic HTML injection, or third-party runtime dependencies.
- Confirmed external links opened in new tabs use `rel="noreferrer"`.
- Remaining manual check: load the site in a browser and exercise the mobile menu, primary links, images, and browser console after deployment.
