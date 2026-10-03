# Receipts website

The public website for [Receipts](https://github.com/Aashutosh31/receipts), a 90-day accountability app built around clear commitments and an honest record.

Live site: <https://aashutosh31.github.io/receipts/>

This is a dependency-free static site. It has no backend, authentication, analytics, or runtime service of its own. The Android app and its data systems live in the separate mobile repository.

## Features

- Responsive, accessible product landing page.
- Real Android app screenshots in `public/images/`.
- Direct APK and GitHub Release links.
- Privacy, security, source, license, robots, and sitemap links.
- Mobile navigation with no third-party JavaScript.

## Project structure

```text
.
├── index.html          # Page structure, metadata, and product copy
├── styles.css          # Responsive visual design
├── script.js           # Mobile navigation behavior
├── public/
│   ├── images/         # Android screenshots
│   ├── favicon.svg
│   ├── robots.txt
│   └── sitemap.xml
├── DEVLOG.md           # Dated implementation and verification notes
└── .gitignore          # Local-only files excluded from Git
```

## Local preview

No package installation is required. From the repository root, run:

```sh
python3 -m http.server 4173
```

Open <http://localhost:4173/> in a browser. The site uses relative asset paths so the same files work both locally and under the GitHub Pages `/receipts/` subpath.

## Deployment

The production URL is <https://aashutosh31.github.io/receipts/>. Publish the repository root through GitHub Pages. Keep the canonical URL in `index.html` and the URL in `public/sitemap.xml` aligned with the live address.

## Verification checklist

Run these checks from the repository root before publishing:

```sh
python3 -m http.server 4173
```

Then verify the page at `/`, test the mobile menu, activate every primary link, and check the browser console and network panel for failed requests. Also confirm that the APK checksum shown on the page matches the intended GitHub Release asset.

The site contains no application secrets. Do not add credentials, private keys, environment files, or generated agent state to the repository.

## Related project

- [Receipts Android source](https://github.com/Aashutosh31/receipts)
- [Privacy policy](https://github.com/Aashutosh31/receipts/blob/main/docs/PRIVACY.md)
- [Security reporting](https://github.com/Aashutosh31/receipts/security/policy)
