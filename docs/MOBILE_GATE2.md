# Mobile Gate 2 — Design & Implementation Notes

## Breakpoint
`@media (max-width: 768px)`

Tablet range (769–959px) keeps the old desktop-hidden behavior.

---

## Hero
- Background: same base64 map image, `background-size: cover; background-position: 50% 22%`
- Gradient overlay: dark bottom fade for text legibility
- Title: 38px / 700, Cinzel (EN) / Noto Sans TC 900 (ZH), manual `<br>` line breaks
- CTA: vertical stack, full-width buttons (52px / 48px)
- Tags: horizontal scroll strip, `overflow-x: auto`, no wrapping

## Island Interaction
- 5 circular tap badges (52×52px) positioned over map
- Positions are approximate (map crops differently at mobile aspect ratio)
- Tap → `openQuestSheet(idx)` → Bottom Sheet
- Bottom Sheet: handle bar, quest number, name, subtitle (lang-aware), Open Demo link, Case Notes button
- Closes on: ✕ button, backdrop tap

**Known:** Badge positions need visual QA on real device. Map crop at `50% 22%` shows center-upper area; n1 (Audio QA) and n3 (Distributor Fit Quiz) are at map edges.

## Featured Live Demos
- `scroll-snap-type: x mandatory`, each card `flex: 0 0 84vw`
- Left/right peek visible to hint scrollability
- Tap card or "Explore All" → Project Gallery Modal

## Core Skills
- 2×3 grid with emoji icon placeholders
- Tap any card → Core Skills Summary Modal (full-screen sheet)

## How I Build
- Vertical step list (no horizontal scroll)
- Step 3 (Build) highlighted as active

## Modals on Mobile
```css
.modal-overlay { align-items: flex-end; }
.modal-card {
  width: 100%;
  max-height: 92vh;
  border-radius: 20px 20px 0 0;
  padding: 24px 20px 40px;
}
```
- `font-size: 16px` on inputs prevents iOS auto-zoom
- Input height: 48px minimum

---

## Open Items for Future Gates

- [ ] Precise island badge positioning (needs device QA)
- [ ] Quest Drawer redesign for mobile (currently opens desktop version)
- [ ] Case Notes content for Quest 03, 04, 05
- [ ] Swipe-to-close gesture on Bottom Sheet
- [ ] "View Process" deep-link target
- [ ] `font-display: swap` on Google Fonts import
- [ ] Actual contact form backend (Tally)
