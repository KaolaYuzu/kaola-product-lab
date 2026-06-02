# Changelog

## Gate 1 Mobile (2026-06-02)
- Added mobile layout `@media (max-width: 768px)`
- Mobile hero: full-screen map background + title + CTA overlay
- Island tap badges (01–05) on mobile map
- Mobile Quest Bottom Sheet with Open Demo / Case Notes
- Featured Live Demos: horizontal scroll card strip on mobile
- Core Skills: 2×3 grid on mobile, tap → Core Skills Modal
- How I Build: vertical step list on mobile
- Modal override: full-screen bottom sheet (92vh, rounded top) on mobile
- iOS zoom fix: form inputs `font-size: 16px`

## Gate 1 Desktop Checkpoint (2026-06-02)
- Desktop layout frozen
- Hero title confirmed: EN "Turn Ideas / into Web Apps / & Web Tools"
- Hero title confirmed: ZH "把想法 / 變成可用 / 網頁工具"

## Typography System (2026-06-02)
- Three-layer font system: Cinzel (EN display) / Montserrat (EN UI) / Noto Sans TC (ZH)
- Google Fonts loaded: Cinzel 700/900, Montserrat 500/600/700, Noto Sans TC 400/500/700/900
- ZH hero override: `html[lang="zh-TW"] .hero-h1` → Noto Sans TC weight 900
- Minimum font-size: 14px global

## i18n & Interaction Fixes (2026-06-02)
- Fixed `toggleLang()` crash: `ctaMap` element removed, added null guard
- Fixed island labels not updating in ZH: applyLang() now includes island getElementById sync
- Added `data-i18n="heroH1"` to h1 element for page-load language sync
- Island sub labels ZH updated to spec: AI 文件重建 / AI 音訊品質保證 / AI 音樂版權文件 / AI 音樂發行路線選擇 / 可重複的 AI 工作流

## Modals & Form (2026-06-02)
- Contact form inputs enabled (removed `disabled`)
- Message Type select: enabled and functional
- Send Message: shows placeholder notice on click (no backend)
- Core Skills Summary Modal added with full EN/ZH content
- Body scroll lock on modal open/release

## Gate 1 Initial Build (2026-06-01)
- Hero map with 5 island nodes
- Quest Drawer (Case Notes) for Quest 01 and 02
- Project Gallery Modal (All Projects)
- About Creator Modal (EN + ZH)
- Contact / Feedback Modal
- Featured Live Demos, Core Skills, How I Build bottom sections
- Full EN / ZH i18n toggle
