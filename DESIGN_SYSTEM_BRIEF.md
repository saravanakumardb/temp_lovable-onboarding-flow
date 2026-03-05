# Design System Brief (Must Follow)

This repo is an onboarding/settings UX pattern source.

## Non-negotiable rules

- No `console.log`.
- No network calls.
- No hardcoded colors (hex/rgb/hsl). Use CSS variables.

## Token usage

- Use `UX_TOKEN_CONTRACT.md`.

## Component architecture

- Reusable components in `src/components/**`.
- Steps/pages in `src/app/**` compose components.
- Components must NOT import from `src/app/**`.

## UX

- Great validation states.
- Keyboard accessible.
- Mobile-first responsive.
