# QA Record — Kaola Product Lab Clean Package

Date: 2026-06-02

## Package QA Status

| Area | Status |
|---|---|
| Desktop Gate 1 | LOCKED |
| GitHub/Vercel entry file | READY (`index.html`) |
| Mobile Gate 2 RC1 | FAILED / DO NOT CONTINUE |
| Mobile Gate 2 RC2 | READY FOR IMPLEMENTATION |
| Old mobile proposal | REMOVED / DEPRECATED |
| Reference assets | CLEANED AND RENAMED |

## Desktop Must Not Break

After any mobile patch, verify:

- desktop hero still matches the locked layout
- desktop island labels remain aligned
- About Creator opens correctly
- Contact / Feedback opens correctly
- Contact fields are editable
- Featured Live Demos opens gallery
- Core Skills opens summary
- EN / 中文 toggle works
- no new desktop layout drift

## Mobile Gate 2 RC1 Failure Summary

RC1 failed because:

- it used a desktop hero crop as the mobile visual base
- markers overlapped the hero title
- mobile information flow was not vertical/mobile-first
- project and skill sections looked like desktop elements compressed into mobile
- the architecture did not match the desired base image + overlay logic

Do not continue RC1 patching.

## Mobile Gate 2 RC2 QA Targets

RC2 must pass:

### Visual / Layout

- mobile layout follows vertical product map page logic
- top map / hero does not feel like desktop cropped into phone
- hero title does not block island map readability
- project cards are readable and touch-friendly
- bottom navigation is stable and not intrusive

### Architecture

- text, icons, markers, nav, cards are HTML/CSS overlay
- no UI text is burned into images
- reference images are used as implementation guidance, not direct full-page screenshots

### Interaction

- Map tab returns to map section
- Projects tab scrolls to project list
- Skills tab scrolls to skill section
- Process tab scrolls to process section
- About tab opens About sheet
- Project cards open detail sheet
- Try Live Demo opens correct external demo where applicable
- View Case Notes uses existing placeholder/available behavior

### Form

- Contact form fields can be typed into on iPhone
- select dropdown can open
- keyboard does not permanently hide the active input
- Send button remains placeholder only unless backend is added later

### i18n

- ZH mode does not show English UI instructions except allowed brand/project/technical terms
- EN mode does not show Chinese UI instructions
- mobile-only text is included in the i18n system

## Completion Rule

A patch is not PASS until Q explicitly says PASS.

