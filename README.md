# Kaola Product Lab — Clean Handoff Package

Date: 2026-06-02  
Package status: CLEANED / DESKTOP LOCKED / MOBILE GATE 2 RC2 READY

## Purpose

This package is the clean handoff base for Kaola Product Lab.

It contains:

- the locked desktop checkpoint
- a GitHub/Vercel-ready `index.html`
- updated mobile reference assets
- cleaned Mobile Gate 2 RC2 implementation specification
- QA and asset manifest files

The goal is to avoid old mobile references, outdated proposal logic, and mixed instructions.

## Current Truth Source

Desktop Gate 1 is the source of truth for:

- brand direction
- project names
- visual worldbuilding
- island order
- desktop interaction
- bilingual content direction
- typography direction

Mobile Gate 2 must be built from this desktop truth source, but using a mobile-first layout.

## Main Files

| File | Purpose |
|---|---|
| `index.html` | GitHub / Vercel entry file. Same content as desktop checkpoint. |
| `index_r7b_gate1_desktop_checkpoint.html` | Locked desktop checkpoint copy. Do not modify unless Q instructs. |
| `README.md` | Clean package overview. |
| `CHECKPOINT_NOTE.md` | Desktop freeze and version note. |
| `QA.md` | QA status and test checklist. |
| `MOBILE_GATE2_RC2_SPEC.md` | Current mobile implementation spec. Use this, not old proposals. |
| `AGENT_HANDOFF_MOBILE_GATE2_RC2.md` | One-file handoff brief for engineering agent. |
| `ASSET_MANIFEST.md` | Reference image usage and naming. |
| `references/` | Current image references. |

## Important Architecture Rule

Mobile must follow the same controllable architecture as desktop:

**base visual image / map background**  
+  
**HTML / CSS overlay for all text, icons, markers, cards, buttons, nav, and interactions**

Do not burn UI text, icons, buttons, cards, markers, or nav into images.

## Desktop Status

Desktop Gate 1 is frozen.

Do not modify:

- desktop hero
- desktop background
- desktop island positions
- desktop typography
- desktop modals
- desktop bottom sections
- desktop i18n

## Mobile Status

Mobile Gate 2 RC1 failed because it treated the desktop layout as a responsive crop.

Mobile Gate 2 RC2 must use the new mobile direction:

**vertical product map page**  
with

- mobile map / hero section
- project quest cards
- Core Skills
- How I Build
- reusable systems
- creative AI production
- final CTA
- fixed bottom navigation

## Deprecated / Do Not Use

Do not use the old `MOBILE_GATE2_PROPOSAL.md` logic from the previous package.

That proposal contained the failed RC1 direction:

- desktop map cropped with `cover`
- badge overlay on hero title
- mobile layout as desktop shrink
- bottom sheet attached to desktop map zones

This package intentionally replaces it with `MOBILE_GATE2_RC2_SPEC.md`.

---

## Agent Team Assignment

For all Mobile Gate 2 RC2 work, read `AGENT_TEAM_ASSIGNMENT.md` before execution.

Required structure:
- 阿得 = Foreman / Lead Coordinator
- Tech Executor = implementation subagent
- QA Inspector = QA subagent

Subagents must report to 阿得.  
阿得 must consolidate and report to Q.  
Only Q can PASS.

