# Delete or overwrite these old files before deploying

To prevent stale browser / Cloudflare / PWA behavior, remove old variants if they exist:

- old `site.webmanifest` references from previous versions are no longer linked from HTML. You may leave the file, but the live `index.html` must not reference it.
- old `favicon.ico` must be replaced with this package's new `favicon.ico`.
- old `kairos-clock-*`, `kairos-clock-icon-*`, and `kairos-clock-fav*` duplicate icon files may be deleted.
- old broken `index.html` must be fully replaced.

After upload:
1. Cloudflare → Caching → Purge Everything.
2. Open `https://runkairos.com/?qa-final=20260702` in Incognito.
3. If Chrome still shows an old K icon inside “Open in app,” uninstall the local Chrome app from `chrome://apps`. That icon is local Chrome app metadata, not the live favicon.
