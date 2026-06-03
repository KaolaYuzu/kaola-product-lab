# R11 Recovery + Formspree Patch
Date: 2026-06-03
Base: R9 (Kaola_MobileGate2_RC2_R9_QPatch_MobileQA_20260603) — last QA-passed build

## What Changed
- **index.html only** — all other files identical to R9

### Desktop contactModal
- Added `id` attributes to 4 form fields: `cf-name`, `cf-email`, `cf-topic`, `cf-message`
- Added honeypot: `<input id="cf-gotcha" type="text" name="_gotcha" hidden>`
- Changed submit button onclick → `submitDesktopContact(event)`
- `cf-notice` div now used for validation / success / error feedback

### Mobile mobileContactModal
- Replaced non-focusable `.mc-display-field` divs with real inputs (no autofocus)
  - `<input id="mc-name">`, `<input id="mc-email">`, `<input id="mc-topic">`
  - `<select id="mc-msgtype">` with 4 options
  - `<textarea id="mc-message">`
- Added honeypot: `<input id="mc-gotcha" type="text" name="_gotcha" hidden>`
- Changed send button onclick → `submitMobileContact(event)`
- `mc-notice` div now used for validation / success / error feedback

### JS added (before </script>)
- `var CONTACT_FORM_ENDPOINT = "https://formspree.io/f/mjgdbela"`
- `_doFormspreeSubmit(data, btnEl, noticeEl)` — shared fetch helper
- `submitDesktopContact(e)` — desktop form handler
- `submitMobileContact(e)` — mobile form handler

## Strictly NOT Changed
- Hero, mobile layout, About Creator modal, Capability Quest, desktop layout
- All CSS / media queries / z-index / overlay / RWD
- modal HTML structure
- All reference images and doc files
