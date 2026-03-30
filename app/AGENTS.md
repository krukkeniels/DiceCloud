# AGENTS.md (app scope)

This file applies to everything under `app/`.

## Technical context
- Framework: Meteor
- UI: Vue 2 + Vuetify 2
- Language mix: JavaScript + TypeScript
- Linting: ESLint (`npm run lint`)
- Tests: Meteor test runner (`npm test`)

## Editing guidelines
- Keep module boundaries intact (`imports/client`, `imports/server`, `imports/api`).
- Prefer small, localized edits over broad refactors.
- Match existing style:
  - single quotes
  - existing naming conventions
  - avoid introducing new patterns unless needed
- Do not change build/tooling config unless the task requires it.

## Validation guidance
- Default validation for code changes:
  1. `npm run lint`
  2. Run targeted tests when possible, or `npm test` when appropriate.
- For documentation-only updates under `app/`, lint/tests are optional.

## Meteor-specific notes
- Run commands from `app/`.
- Typical local startup: `meteor npm install` then `meteor`.
- Use settings files/environment variables as documented in the root `README.md`.

## Performance and risk
- Avoid unnecessary reactive recomputation in UI code.
- Be careful with publication/subscription changes; prefer additive safe changes.
- For schema or migration updates, document rollout considerations.

