# AGENTS.md

This file defines guidance for AI coding agents working anywhere in this repository.

## Project snapshot
- Repo: **DiceCloud**
- Runtime: Meteor + Node.js app in `app/`
- Main entrypoint for local dev: run Meteor from the `app/` directory.

## Goals for agent contributions
- Keep changes **small, focused, and reversible**.
- Prefer fixing root causes over adding workarounds.
- Preserve current behavior unless a task explicitly requests a behavior change.
- Leave clear notes in commit messages and PR descriptions about what changed and why.

## Workflow expectations
1. Read this file and any deeper `AGENTS.md` files before editing.
2. Inspect relevant files before patching; avoid repo-wide speculative edits.
3. Make minimal code/documentation changes needed for the task.
4. Run the narrowest meaningful validation command(s).
5. Summarize changes and validation results clearly.

## Safety guardrails
- Never commit secrets, API keys, private tokens, or `.env` contents.
- Do not add new dependencies unless required by the task.
- Avoid destructive data operations in scripts or migrations unless requested.
- If requirements are ambiguous, choose the least risky interpretation and call it out.

## Validation defaults
- For docs-only changes: no runtime checks required.
- For code changes in `app/`: follow `app/AGENTS.md` for lint/test guidance.

## Commit and PR quality bar
- Use concise, imperative commit titles (e.g., `docs: add agent workflow guidance`).
- PR descriptions should include:
  - What changed
  - Why it changed
  - How it was validated
  - Any follow-up work or risks

