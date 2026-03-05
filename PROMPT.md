# Lovable App 3 — Onboarding + Settings Wizard (Micro-App)

Before you start: read and follow `DESIGN_SYSTEM_BRIEF.md`.

## Goal

Build a best-in-class **onboarding + settings wizard** micro-app demonstrating premium UX patterns we can reuse across products.

## Constraints

- Only modify files in this repository.
- No backend calls; localStorage only
- No `console.log`
- No hardcoded colors (CSS variables)

## Experience requirements (high polish)

### Onboarding flow

- Multi-step wizard (5–7 steps)
- Progress indicator + step labels
- Back/Next with validation
- Optional “Skip for now” with confirm dialog
- Autosave progress to localStorage

### Steps to include (example)

- Profile basics (name, timezone)
- Preferences (theme, density)
- Notifications (toggles)
- Integrations (fake list, connect buttons)
- Privacy level selector
- Final review summary

### Settings area

After onboarding completes, show a settings dashboard with:

- profile card
- preferences section
- notification settings
- danger zone (delete local profile) with confirm

### UX/accessibility

- Great empty/error/validation states
- Keyboard accessible
- Mobile-first responsive

## Routes

- `/` start/resume onboarding
- `/onboarding` wizard
- `/settings` settings dashboard

## Deliverables

- Next.js 16 App Router
- Tailwind v4
- TypeScript strict
- Scripts: `dev`, `check`, `build` (`next build --webpack`)

## Success criteria

- Feels like a premium consumer app onboarding
- Components reusable in other products
- Safe and self-contained
