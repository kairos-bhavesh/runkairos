# Kairos Fixed Release v2

Fixes applied:
- Removed the broken inline html2pdf bundle that contained a literal `</script>` sequence and caused minified JavaScript + 404 output to render on the page.
- Kept PDF functions functional through the safe browser fallback instead of breaking the page.
- Added a robust Request Demo handler that works from the site, app overlay, and demo lock screen.
- Added a robust Back to site handler for the demo lock screen.
- Added cache-busted favicon / PWA icon references so browsers stop showing the old app icon.
- Added 192x192 and 512x512 PWA icons based on the clock logo.

Deployment:
1. Upload every file in this folder to the website root.
2. Replace the existing index.html, site.webmanifest, favicon files, and icons.
3. In Cloudflare, Purge Everything.
4. In Chrome, remove the old installed web app / shortcut if it still shows the old icon, then reopen the site.
