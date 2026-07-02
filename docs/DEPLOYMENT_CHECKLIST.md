# Deployment Checklist

1. Upload the full package to the root of `runkairos.com`.
2. Replace old files, especially `favicon.ico`, `site.webmanifest`, `index.html`, and `html2pdf.bundle.min.js`.
3. Cloudflare → Caching → Purge Everything.
4. Test in Incognito: `https://runkairos.com/?enterprise=20260702`.
5. In the page source, search for `favicon.ico`, `manifest`, and `FAB`.
   - `favicon.ico` should not be referenced by HTML.
   - `manifest` should not be linked by HTML.
   - `FAB` should not appear as a client reference.
6. Click Request Demo from the header.
7. Click Explore Live Platform, then Back to site.
8. If Chrome still shows old "Open in app", uninstall the old Chrome app for `runkairos.com` and reload.
