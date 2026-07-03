# Kairos v1.2 Full QA Fixed

Fixes included:
- Removed the inline html2pdf bundle that contained literal `</script>` strings and caused JavaScript code to render visibly on the page.
- Moved html2pdf to `/html2pdf.bundle.min.js`.
- Fixed Request Demo links from every state.
- Fixed Back to Site from private demo gate and app overlay.
- Added safe PDF fallback that downloads HTML rather than dumping library code or 404 content into the page.
- Removed PWA manifest link from the HTML to prevent Chrome from surfacing stale installed-app icon metadata.
- Rebuilt clock-only favicon and PNG icon set.
- Added cache-busted icon references.

Deployment:
1. Upload all files to the website root.
2. Delete old files not in this package if possible, especially old manifest/icon variants.
3. Cloudflare: Purge Everything.
4. Chrome: test in Incognito with `https://runkairos.com/?qa-final=20260702`.
5. If the browser still shows an old Open in app icon, uninstall the old Chrome app from `chrome://apps`; this is local Chrome metadata.
