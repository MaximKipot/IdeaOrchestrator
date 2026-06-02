---
name: idea-o-06-principles
description: Use when defining decision principles, constraints, preferences, and boundaries.
---

# Principles Constraints

## Quick Start

1. Read current state, direction, and anti-vision.
2. Create only `06-principles` files if missing.
3. Write 3-7 actionable principles.
4. Separate constraints from preferences.
5. Update current state and route forward.

## Context Budget

Always read:

- `00-control/current-state.md`
- `05-vision-direction/direction.md`

Read only if needed:

- `05-vision-direction/anti-vision.md`
- `06-principles/principles.md`
- `06-principles/constraints.md`

Do not read:

- strategy files unless checking conflict
- future phase folders

Resolve `framework/rules/...` from the project workspace first, then from the installed IDEA-O skill/framework location. Missing project-local rules are not a failure.

Read `framework/rules/context-efficiency.md` only when unsure what to load.

## Ease Of Use Rules

- Ask only questions that block the next useful file update.
- Create only files needed for the current action.
- Keep outputs compact: bullets or tables, not long narrative.
- Preserve uncertainty labels and rejected alternatives.
- Keep `00-control/current-state.md` as a compact dashboard with active decisions, blocking questions, recently changed files, and next action; move long history elsewhere.
- Use decision lifecycle statuses in `00-control/decision-log.md`: Active, Superseded, Rejected, Deferred, Archived.
- Triage `00-control/open-questions.md` into Blocking Next Action, Decision Needed Soon, Research Later, Parking Lot, and Resolved.


## Persistence Rules

- Before writing, check `00-control/current-state.md`, unresolved `00-control/open-questions.md`, and existing phase files for what the user already completed, deliberately skipped, or left blocked.
- Treat a phase as unfinished until required outputs are written to files or consciously skipped with accepted risk.
- If required output is missing, keep going by updating the file, asking one blocking question, or logging a conscious skip.
- Do not mark the phase complete or recommend the next skill until outputs exist or each missing output has reason, risk, owner, date, and revisit trigger.
- If the user asks to skip or jump, state the risk briefly and record explicit acceptance before advancing.

## When To Use

Use for phase `06-principles-constraints`.

## Inputs

- Direction
- Anti-vision
- Known constraints
- User preferences

## Files To Read

- `00-control/current-state.md`
- `05-vision-direction/direction.md`
- `05-vision-direction/anti-vision.md`

## Files To Write

- `06-principles/principles.md`
- `06-principles/constraints.md`
- `00-control/decision-log.md` if needed
- `00-control/current-state.md`
- `00-control/handoff.md` when Clean Handoff Mode is active

## Questions To Ask

- What principles guide tradeoffs?
- Which constraints are hard?
- Which are preferences?

## Blocking Conditions

- Constraints are unknown and affect strategy.
- Principles are too vague to guide decisions.

## Skip Behavior

Log risk that future choices may be inconsistent.

## Outputs

- Actionable principles
- Classified constraints
- Constraint decisions if any

## Quality Gate

Before marking this phase complete, apply `framework/rules/phase-quality-gates.md`. Do not complete the phase until required files, decisions, open questions, skip risks, evidence labels, rejected alternatives, current state, and handoff requirements are handled.

## Handoff Output

When Clean Handoff Mode is active, update `00-control/handoff.md` using `framework/rules/clean-handoff.md`. Include completed phase, files updated, confirmed decisions, key facts, key assumptions, open questions, skipped risks, recommended next skill, and minimum files the next skill must read.

## Next Recommended Skill

`idea-o-07-strategy`
