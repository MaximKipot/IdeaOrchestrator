---
name: idea-o-review
description: Use when reviewing evidence, experiment results, stalls, or deciding whether to continue, adjust, pivot, pause, or stop.
---

# Review Pivot

## Quick Start

1. Read current state, experiment design, metrics, and progress.
2. Create only `11-review` files if missing.
3. Summarize what changed and what was learned.
4. Decide continue, adjust, pivot, pause, or stop.
5. Update current state and route next.

## Context Budget

Always read:

- `00-control/current-state.md`
- `10-execution/progress-log.md`

Read only if needed:

- `08-mvp-experiments/experiment-design.md`
- `07-strategy/success-metrics.md`
- `03-research/evidence-map.md`
- `11-review/*`

Do not read:

- templates/
- examples/
- future phase folders

Read `framework/rules/context-efficiency.md` only when unsure what to load.

## Ease Of Use Rules

- Ask only questions that block the next useful file update.
- Create only files needed for the current action.
- Keep outputs compact: bullets or tables, not long narrative.
- Preserve uncertainty labels and rejected alternatives.

## When To Use

Use for phase `11-review-pivot`.

## Inputs

- Progress log
- Experiment design
- Success metrics
- Evidence map
- User judgment

## Files To Read

- `00-control/current-state.md`
- progress log
- experiment design and metrics if needed

## Files To Write

- `11-review/review-log.md`
- `11-review/pivot-decisions.md`
- `09-roadmap/rejected-options.md` if preserving paths
- `00-control/decision-log.md`
- `00-control/current-state.md`
- `00-control/handoff.md` when Clean Handoff Mode is active

## Questions To Ask

- What did the evidence show?
- Should the project continue, adjust, pivot, pause, or stop?
- What should be preserved?

## Blocking Conditions

- No evidence or progress to review.
- Pivot proposed without consequences.

## Skip Behavior

Log risk that the project may continue despite contradictory evidence.

## Outputs

- Review findings
- Continue/pivot/pause/stop decision
- Preserved alternatives
- Updated current state

## Quality Gate

Before marking this phase complete, apply `framework/rules/phase-quality-gates.md`. Do not complete the phase until required files, decisions, open questions, skip risks, evidence labels, rejected alternatives, current state, and handoff requirements are handled.

## Handoff Output

When Clean Handoff Mode is active, update `00-control/handoff.md` using `framework/rules/clean-handoff.md`. Include completed phase, files updated, confirmed decisions, key facts, key assumptions, open questions, skipped risks, recommended next skill, and minimum files the next skill must read.

## Next Recommended Skill

`idea-o` to route the next phase or action.
