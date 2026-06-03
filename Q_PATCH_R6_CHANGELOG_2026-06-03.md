# Q Patch R6 — Mobile Hero Legibility + Security Headers

Date: 2026-06-03
Base: Mobile Gate 2 RC2 R5 QPatch

## Changed files

- `index.html`
- `vercel.json`
- `SECURITY_HEADERS_NOTE_2026-06-03.md`
- `Q_PATCH_R6_CHANGELOG_2026-06-03.md`

## Mobile UI patch

- Increased mobile hero subtitle size and contrast.
- Increased mobile hero button height and button text size.
- Added language-aware mobile button sizing for Chinese and English.
- Kept the mobile hero artboard, map image, islands, glowing path, ship, treasure chest, hotspot logic, nav, Contact modal, and desktop checkpoint unchanged.

## Security patch

- Added Vercel HTTP security headers via `vercel.json`.
- CSP intentionally deferred to avoid breaking external links or future third-party integrations.

## QA focus

- Test mobile widths: 390, 443, 577, 630.
- Check EN/ZH hero subtitle and buttons are readable.
- Check treasure chest remains visible.
- Check desktop regression.
- After deployment, verify response headers in DevTools Network panel.
