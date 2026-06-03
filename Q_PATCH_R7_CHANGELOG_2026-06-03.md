# Q PATCH R7 CHANGELOG — Mobile QA Hotfix

Date: 2026-06-03
Status: GitHub Preview Candidate
Scope: `index.html` only

## Fixed

1. Mobile hero English body line break
   - Adjusted the English hero body so `This is my / capability map.` breaks cleanly instead of visually splitting awkwardly.

2. Mobile hero CTA tap behavior
   - Added explicit `type="button"`, `preventDefault()`, and `stopPropagation()` to mobile hero buttons.
   - Added blur safety before opening modals to avoid iOS keyboard / autofill hijacking.

3. Mobile Contact / Feedback sheet
   - Converted the mobile-only contact sheet from focusable form inputs into non-focusable preview fields.
   - This prevents iOS Safari from opening the keyboard / AutoFill bar when the Contact / Feedback button is tapped.
   - Desktop `contactModal` remains untouched.

4. Capability Quest image layer alignment
   - Fixed the mobile `mobileBG1-2.png` sprite sizing.
   - Previous scaling compressed five panels into `1000px`, causing adjacent panels to bleed into cards and appear like two misaligned layers.
   - Updated to native `1754px` sprite height and corrected background positions for all five Quest cards.

## Not changed

- Desktop Gate 1 checkpoint
- Hero map image `mobileBG1-1.png`
- Island artwork
- Light path / boat / treasure chest
- Vercel security headers
- Core navigation and language toggle logic
