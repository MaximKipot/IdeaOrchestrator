---
name: vision-direction
description: Use when turning evidence and uncertainty into vision, direction, and anti-vision.
---

# Vision Direction

## Quick Start

1. Read current state, problem, evidence, assumptions, and risks.
2. Create only `05-vision-direction` files if missing.
3. Draft vision, direction, and anti-vision.
4. Log direction decisions.
5. Update current state and route forward.

## Context Budget

Always read:

- `00-control/current-state.md`
- `02-problem/problem-context.md`
- `03-research/evidence-map.md`

Read only if needed:

- `04-assumptions-risks/assumptions.md`
- `04-assumptions-risks/risks.md`
- `05-vision-direction/*`

Do not read:

- strategy files unless direction already exists
- future phase folders

Read `framework/rules/context-efficiency.md` only when unsure what to load.

## Ease Of Use Rules

- Ask only questions that block the next useful file update.
- Create only files needed for the current action.
- Keep outputs compact: bullets or tables, not long narrative.
- Preserve uncertainty labels and rejected alternatives.

## When To Use

Use for phase `05-vision-direction`.

## Inputs

- Problem context
- Evidence map
- Assumptions and risks
- User preferences

## Files To Read

- `00-control/current-state.md`
- `02-problem/problem-context.md`
- `03-research/evidence-map.md`
- assumptions/risks if needed

## Files To Write

- `05-vision-direction/vision.md`
- `05-vision-direction/direction.md`
- `05-vision-direction/anti-vision.md`
- `00-control/decision-log.md`
- `00-control/current-state.md`
- `00-control/handoff.md` when Clean Handoff Mode is active

## Questions To Ask

- What future should this create?
- Which direction fits the evidence?
- What should it avoid becoming?

## Blocking Conditions

- Direction depends on unresolved critical assumptions.
- Direction conflicts with constraints.

## Skip Behavior

Log risk of ambiguous direction or scope creep.

## Outputs

- Vision
- Direction decision
- Anti-vision
- Deferred or rejected directions

## Quality Gate

Before marking this phase complete, apply `framework/rules/phase-quality-gates.md`. Do not complete the phase until required files, decisions, open questions, skip risks, evidence labels, rejected alternatives, current state, and handoff requirements are handled.

## Handoff Output

When Clean Handoff Mode is active, update `00-control/handoff.md` using `framework/rules/clean-handoff.md`. Include completed phase, files updated, confirmed decisions, key facts, key assumptions, open questions, skipped risks, recommended next skill, and minimum files the next skill must read.

## Next Recommended Skill

`principles-constraints`
