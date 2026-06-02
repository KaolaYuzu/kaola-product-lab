# QA Record

## Gate 1 Desktop — Completed ✅

### Hero
- [x] Background image (base64 inline)
- [x] EN title: "Turn Ideas / into Web Apps / & Web Tools" (manual `<br>`)
- [x] ZH title: "把想法 / 變成可用 / 網頁工具" (manual `<br>`, Noto Sans TC 900)
- [x] Hero body copy EN + ZH
- [x] CTA: About Creator (primary) + Contact / Feedback (secondary)
- [x] Hero tags horizontal strip
- [x] Quest hint top-right EN + ZH

### Island Map
- [x] 5 island nodes, click → Quest Drawer
- [x] Island labels EN + ZH (name + subtitle)
- [x] ZH subtitles: AI 文件重建 / AI 音訊品質保證 / AI 音樂版權文件 / AI 音樂發行路線選擇 / 可重複的 AI 工作流
- [x] toggleLang() null-guard (ctaMap removed)
- [x] applyLang() island label sync on page load

### Modals
- [x] About Creator (EN + ZH, scroll)
- [x] Contact / Feedback (fields enabled, Send placeholder)
- [x] Core Skills Summary (EN + ZH, 6 modules)
- [x] Project Gallery (5 quests, EN + ZH)
- [x] Body scroll lock

### Bottom Sections
- [x] Featured Live Demos (3 cards, click → Gallery Modal)
- [x] Core Skills (6 icon cards, click → CS Modal)
- [x] How I Build (5 steps)
- [x] Section titles i18n EN + ZH
- [x] Small links i18n EN + ZH

### Typography
- [x] Cinzel / Montserrat / Noto Sans TC loaded
- [x] ZH hero: Noto Sans TC 900 via `html[lang="zh-TW"]`
- [x] Min font-size: 14px

### i18n
- [x] Full EN/ZH toggle
- [x] ZH: no English UI text (brand names + skill tags excepted)
- [x] EN: no Chinese text

---

## Gate 1 Mobile — Initial ✅

### Mobile Hero
- [x] Map background (cover, 50% 22%)
- [x] Title EN + ZH with manual line breaks
- [x] CTA buttons (primary + secondary), full-width
- [x] Hero tags horizontal scroll

### Island Interaction
- [x] 5 tap badges (52×52px), approximate map positions
- [x] openQuestSheet(idx) → Bottom Sheet
- [x] Bottom Sheet: Quest num, name, sub (EN/ZH), Open Demo, Case Notes
- [x] Backdrop tap closes sheet

### Bottom Sections (Mobile)
- [x] Featured Demos: horizontal scroll strip, 84vw cards
- [x] Core Skills: 2×3 grid, tap → CS Modal
- [x] How I Build: vertical step list

### Modals (Mobile)
- [x] Full-screen bottom sheet (92vh, 20px top radius)
- [x] iOS zoom fix (font-size: 16px on inputs)
- [x] Input height 48px

---

## Known Issues / Watch Items

1. **Island badge positions** — approximate; needs visual QA on real device
2. **Google Fonts offline** — fallback to system fonts, layout intact
3. **Quest Case Notes 03–05** — placeholder state, content TBD
4. **Contact form** — no backend; Send Message shows notice only
5. **`& Web Tools`** — uses `&amp;` in i18n, renders correctly via innerHTML
6. **View All / View Process** — currently static `#` links (no deep-link target)
7. **Quest Drawer on mobile** — desktop Drawer CSS not redesigned for mobile; Gate 2.1 scope
