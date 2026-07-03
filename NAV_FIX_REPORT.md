# Kairos v1.3 Navigation Fix

## Issue found
The final QA stabilizer had overridden `closeAppAndScroll(sectionId)` so it always scrolled to the Demo section, ignoring the requested `sectionId`. This caused all top navigation links to feel unlinked or wrong.

## Fix applied
- Restored section-aware scrolling for:
  - The Problem → `#problem`
  - Why KAIROS → `#why-kairos`
  - Platform in Action → `#platform`
  - Decision & Behavioral Science → `#decision-science`
  - Outcomes → `#outcomes`
  - Security → `#security`
  - Request Demo → `#demo`
- Added robust event delegation for header navigation.
- Added mobile menu close behavior after selecting a link.
- Kept Request Demo flow reliable from any page state.

## Test after deploy
Use: `https://runkairos.com/?navfix=20260703`
Then click every top nav item and confirm each moves to the correct section.
