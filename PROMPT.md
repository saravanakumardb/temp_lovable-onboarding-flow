# Lovable — Onboarding + Settings Wizard

**GitHub repo:** `saravanakumardb/temp_lovable-onboarding-flow`

## Push Instructions

- Push directly to `main` — do NOT open a PR
- Only modify files in this repo

## Rules

- No `console.log`
- No network calls — mock data / localStorage only
- No hardcoded colors — no hex, no rgb/rgba/hsl, no `bg-[#123456]` Tailwind classes
- Do NOT commit `.env*`, `.next/`, `node_modules/`, `.vercel/`
- pnpm only
- `pnpm run check` must pass (`tsc --noEmit` + `eslint`)
- `pnpm run build` must pass (`next build --webpack`)

## CSS Token Contract

Define in `src/app/globals.css` under `:root` (add `.dark` override):

- `--ux-bg` — page background
- `--ux-surface` — card/panel surface
- `--ux-surface-2` — elevated surface
- `--ux-border` — borders
- `--ux-text` — primary text
- `--ux-text-muted` — secondary text
- `--ux-accent` — primary accent
- `--ux-accent-foreground` — text on accent
- `--ux-danger` — destructive/error
- `--ux-warning` — warning
- `--ux-success` — success
- `--ux-ring` — focus ring
- `--ux-shadow` — shadows

Use only via Tailwind: `bg-[var(--ux-surface)]`, `text-[var(--ux-text)]`, `border-[var(--ux-border)]`

## Component Architecture

- Reusable components → `src/components/`
- Pages in `src/app/**` compose components only
- Components must NOT import from `src/app/**`

## Stack

- Next.js 16 App Router, React 19, TypeScript strict
- TailwindCSS v4, pnpm

## Goal

Build a best-in-class **onboarding + settings wizard** micro-app with premium UX patterns reusable across ByteLyst products. Feels like a premium consumer app. Design-led.

Data: localStorage only — no backend calls.

## Pages

- `/` start / resume onboarding
- `/onboarding` wizard
- `/settings` settings dashboard

## Onboarding Flow

Multi-step wizard (5–7 steps):

- Progress indicator + step labels
- Back/Next with validation
- "Skip for now" with confirm dialog
- Autosave to localStorage

Steps: profile basics (name, timezone), preferences (theme, density), notifications (toggles), integrations (fake list), privacy level, final review summary

## Settings Dashboard

After onboarding: profile card, preferences, notification settings, danger zone (delete local profile with confirm dialog)

## UX/Accessibility

Great empty/error/validation states, keyboard accessible, mobile-first responsive

## Verification

```
pnpm install && pnpm run check && pnpm run build
```
