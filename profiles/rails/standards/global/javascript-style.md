# JavaScript & Stimulus Style Guide

Lightweight standards for Hotwire front-end work. Use Prettier/ESLint for enforcement.

## Core Principles
- Progressive enhancement first: HTML/Tailwind baseline, Stimulus adds behavior.
- One Stimulus controller per concern; expose clear `targets`, `values`, and event handlers.
- Prefer modular utilities in `app/javascript/lib/` instead of repeating DOM helpers.
- Ship ES modules (`import`/`export`) and avoid globals.
- Bake accessibility in (focus states, ARIA attributes, keyboard support).

## Controllers
- Keep controllers short; delegate heavy logic to services or utilities.
- Register `targets`, `values`, and `classes` explicitly; document expected markup in comments.
- Guard against missing DOM elements to prevent runtime errors.
- Use Stimulus actions instead of inline JS; wire analytics/logging through shared helpers.

## Utilities & Modules
- One utility per file with named exports; keep functions pure where possible.
- Co-locate tests (Vitest/Jest) for non-trivial utilities.
- Document tricky helpers with brief JSDoc including params/returns.

## Formatting & Naming
- camelCase variables/functions, PascalCase classes/controllers, SCREAMING_SNAKE_CASE constants.
- Keep functions under ~15 lines; extract helpers when branching increases.
- Prefer template literals for string interpolation; single quotes elsewhere.
- Use descriptive event handler names (`handleSubmit`, `toggleModal`).

## Comments & Documentation
- Comment why a workaround exists (browser quirk, API constraint); omit obvious narration.
- Use `TODO:` with owner/issue references only when work is intentionally deferred.
- Keep README snippets/examples up to date when controllers change public behavior.
