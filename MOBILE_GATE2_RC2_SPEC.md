# Mobile Gate 2 RC2 Specification

Status: READY FOR IMPLEMENTATION  
Date: 2026-06-02  
Owner: Q

## Core Decision

Mobile Gate 2 RC2 must not continue RC1.

RC2 must rebuild the mobile layout direction using the updated desktop truth source and the new mobile references.

## Build Logic

Mobile must use the same controllable architecture as desktop:

**base visual layer**  
+  
**HTML / CSS overlay layer**

All text, icons, markers, project cards, buttons, bottom navigation, modals, and interactive elements must be implemented in HTML/CSS.

Do not burn UI text or icons into the background image.

## Source of Truth

Use these files:

1. `index_r7b_gate1_desktop_checkpoint.html`  
   Source of desktop truth and current content.

2. `references/desktop_final_source_of_truth_2026-06-02.png`  
   Visual source for current desktop direction.

3. `references/mobile_reference_with_text_2026-06-02.png`  
   Reference for mobile layout, IA, and visual hierarchy.

4. `references/mobile_reference_no_text_no_icon_2026-06-02.png`  
   Reference for layer separation and overlay logic.

Do not use old mobile references as current content.

## Mobile Information Architecture

Mobile layout should follow:

1. Top Header
2. Mobile Map / Hero
3. Capability Quest / Project Cards
4. Featured / Live Demos if needed
5. Core Skills
6. How I Build
7. Reusable Delivery Systems
8. Creative AI Production
9. Final CTA
10. Fixed Bottom Navigation

## Top Header

Include:

- Kaola Product Lab logo / brand
- descriptor: AI Product · QA · Web App or localized equivalent
- EN / 中文 language toggle
- menu icon

Mobile header must be compact and readable.

## Mobile Hero / Map

Hero content:

EN:

Turn Ideas  
into Web Apps  
& Web Tools

ZH:

把想法  
變成可用  
網頁工具

Rules:

- Do not let title overlap important island/map content.
- Do not use one-character-per-line Chinese breaks.
- Do not use desktop hero crop if it causes broken composition.
- If a mobile-specific map base image is available, use it.
- If not, use CSS carefully and keep the map readable.
- Quest markers should look like intentional map markers, not debug badges.

## Capability Quest / Project Cards

Section title:

EN: Capability Quest · 5 Projects  
ZH: 能力任務 · 5 個專案

Project list must use the latest project order:

1. PhotoCheck Docs  
   ZH subtitle: AI 文件重建  
   EN subtitle: Document Intelligence / AI Document Reconstruction

2. Audio QA  
   ZH subtitle: AI 音訊品質保證  
   EN subtitle: AI Audio Quality Assurance

3. Proof of Rights  
   ZH subtitle: AI 音樂權利文件  
   EN subtitle: AI Music Rights Documentation

4. Distributor Fit Quiz  
   ZH subtitle: AI 音樂發行路線選擇  
   EN subtitle: AI Music Release Path / Distributor Matching

5. Skill System  
   ZH subtitle: 可重複的 AI 工作流  
   EN subtitle: Repeatable AI Workflow

Each card should include:

- Quest number
- project visual / thumbnail
- project name
- subtitle
- short description
- tags
- primary CTA
- secondary CTA

## Quest Detail Sheet

Opening a project card or map marker should open a mobile-specific detail sheet.

Do not use desktop drawer.

Detail sheet should include:

- Quest badge
- project name
- subtitle
- visual panel
- What it solves
- My Role
- Skill Badges
- Status
- Try Live Demo
- View Case Notes
- Back to Map

## Bottom Navigation

Fixed bottom navigation:

- Map
- Projects
- Skills
- Process
- About

Behavior:

- Map: scroll to map/hero
- Projects: scroll to project cards
- Skills: scroll to Core Skills
- Process: scroll to How I Build
- About: open About Creator sheet

## Core Skills

Use mobile-first icon grid, not compressed desktop cards.

Core skills may include:

- Product Thinking
- Workflow Design
- AI-assisted Development
- UX / Mobile QA
- QA System Design
- Launch Checklist
- Security Review
- Handoff & Docs
- Human-in-the-loop

## How I Build

Use a compact step flow:

1. Idea
2. Spec
3. Prototype
4. QA
5. Demo
6. Handoff

ZH equivalent should be included in i18n.

## About / Contact

Use full-screen or 92vh bottom sheet on mobile.

Contact form requirements:

- input height at least 48px
- can type into fields
- select dropdown works
- textarea works
- keyboard does not permanently block active field
- Send remains placeholder only unless backend is added later

## Typography

Minimum readable text: 14px.

Recommended:

- Hero title: 34–40px depending on layout
- Section title: 20–24px
- Project title: 18–20px
- Body: 15–16px
- Tags / small labels: minimum 14px

Chinese text must not be too light, too small, or too thin.

## i18n

All mobile-only text must be covered by EN / ZH.

Allowed mixed-language exceptions:

- brand name
- project names
- AI / Web App / QA if used as technical terms
- skill tags when intentionally kept bilingual

## Non-Negotiable Constraints

Do not modify desktop.

Do not change:

- desktop hero
- desktop island positions
- desktop modal behavior
- desktop bottom sections
- desktop typography
- desktop i18n

If shared code must be touched, report exactly what changed and verify desktop.

## Completion Requirement

After implementation, report:

- files modified
- mobile architecture implemented
- desktop unchanged verification
- ZH / EN verification
- interaction verification
- known risks

Do not mark PASS. Q decides PASS.

