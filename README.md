# KAIROS v1 Enterprise Production Release

This package is the stabilized KAIROS website release.

## What changed
- Clock logo is the only favicon/app icon source.
- HTML no longer links the PWA manifest, preventing new stale "Open in app" prompts.
- `site.webmanifest` is still included for future use, but is not linked by `index.html`.
- Request Demo and Back to site are hardened with a production patch.
- The PDF helper bundle is included so PDF actions do not render broken JavaScript/404 text.
- SEO files, Open Graph image, robots.txt and sitemap.xml are included.

## Deploy
Upload every file and folder to the website root. Replace existing files.

## Important Chrome note
If Chrome already shows "Open in app" with the old K icon, that is a previously installed Chrome app for this domain. Uninstall it once from Chrome Apps or the browser address-bar app icon. Website file changes alone cannot remove a locally installed app badge.
