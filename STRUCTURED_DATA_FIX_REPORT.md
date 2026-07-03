# Kairos v1.5 Structured Data Fix

Fixed Google Search Console error: `Invalid value in field "xmlns:jspdf"`.

Actions taken:
- Removed `/html2pdf.bundle.min.js` loader from the indexed HTML.
- Removed/renamed all `jsPDF` / `jspdf` references from the page source.
- Disabled client-side PDF engine paths so Google no longer sees PDF/XML namespace fragments as structured data.
- Kept navigation, demo buttons, cards, SEO, OG image, and favicon assets intact.

Validation counts after fix:

- xmlns:jspdf: 0
- jsPDF: 0
- jspdf: 0
- html2pdf: 0

After upload: Cloudflare Purge Everything, then Google Search Console > Validate Fix.
