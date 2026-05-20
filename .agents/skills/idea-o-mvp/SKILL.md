---
name: idea-o-mvp
description: Use when generating MVP options, experiment options, or selecting the smallest useful next experiment.
---

# MVP Experiments

## Quick Start

1. Read current state, assumptions, risks, target user, and metrics.
2. Create only `08-mvp-experiments` files if missing.
3. Generate at least three options.
4. Select smallest useful experiment.
5. Preserve rejected options and route forward.

## Context Budget

Always read:

- `00-control/current-state.md`
- `04-assumptions-risks/assumptions.md`
- `07-strategy/target-user.md`

Read only if needed:

- `04-assumptions-risks/risks.md`
- `07-strategy/success-metrics.md`
- `06-principles/constraints.md`
- `08-mvp-experiments/*`

Do not read:

- roadmap files until selection is made
- future phase folders

Read `framework/rules/context-efficiency.md` only when unsure what to load.

## Ease Of Use Rules

- Ask only questions that block the next useful file update.
- Create only files needed for the current action.
- Keep outputs compact: bullets or tables, not long narrative.
- Preserve uncertainty labels and rejected alternatives.

## When To Use

Use for phase `08-mvp-experiments`.

## Inputs

- Assumptions
- Risks
- Target user
- Metrics
- Constraints

## Files To Read

- `00-control/current-state.md`
- assumptions/risks
- target user/metrics
- constraints if needed

## Files To Write

- `08-mvp-experiments/mvp-options.md`
- `08-mvp-experiments/smallest-useful-experiment.md`
- `08-mvp-experiments/experiment-design.md`
- `09-roadmap/rejected-options.md` when rejecting options
- `00-control/decision-log.md`
- `00-control/current-state.md`
- `00-control/handoff.md` when Clean Handoff Mode is active

## Questions To Ask

- What are at least three ways to test?
- Which assumption does each test?
- What is the smallest useful experiment?

## Blocking Conditions

- Only one option considered.
- Selected experiment does not test an important assumption.
- Success criteria missing.

## Skip Behavior

Log risk of premature commitment if alternatives are skipped.

## Outputs

- MVP options
- Selected smallest useful experiment
- Experiment design
- Rejected options

## Quality Gate

Before marking this phase complete, apply `framework/rules/phase-quality-gates.md`. Do not complete the phase until required files, decisions, open questions, skip risks, evidence labels, rejected alternatives, current state, and handoff requirements are handled.

## Handoff Output

When Clean Handoff Mode is active, update `00-control/handoff.md` using `framework/rules/clean-handoff.md`. Include completed phase, files updated, confirmed decisions, key facts, key assumptions, open questions, skipped risks, recommended next skill, and minimum files the next skill must read.

## Next Recommended Skill

`idea-o-roadmap`
