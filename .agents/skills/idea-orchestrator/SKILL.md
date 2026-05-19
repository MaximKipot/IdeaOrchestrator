---
name: idea-orchestrator
description: Use when starting or continuing an idea project, choosing the next phase, handling phase jumps, or checking overall framework progress.
---

# Idea Orchestrator

## When To Use

Use before any phase, when resuming a project, or when the user asks what to do next.

## Inputs

- User request
- Project files
- Desired depth override, if any

## Files To Read

- `AGENTS.md`
- `framework/rules/phase-transition-rules.md`
- `00-control/current-state.md`
- `00-control/open-questions.md`
- `00-control/decision-log.md`

## Files To Write

- `00-control/current-state.md`
- `00-control/open-questions.md`
- `00-control/decision-log.md` when process decisions are made

## Questions To Ask

- Are you starting a new idea or continuing an existing one?
- Do you want to follow the next recommended phase or jump somewhere specific?
- Should this use Light, Standard, or Deep depth?

## Blocking Conditions

- No project files exist.
- `00-control/current-state.md` is missing and the project is not being initialized.
- The requested jump would ignore an unresolved blocker without user acceptance.

## Skip Behavior

If the user skips a phase or jumps ahead, log the skipped phase, reason, risk, owner, and revisit trigger in `00-control/current-state.md`.

## Outputs

- Current phase confirmed
- Depth confirmed
- Blockers identified
- Next recommended skill named

## Next Recommended Skill

Use the phase skill matching the current phase.

