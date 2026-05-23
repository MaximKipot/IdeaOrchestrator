---
name: idea-o-09-roadmap
description: Use when selecting the path, preserving rejected options, and turning an experiment into a practical roadmap.
---

# Decision Roadmap

## Quick Start

1. Read current state and selected experiment.
2. Create only `09-roadmap` files if missing.
3. Record selected path.
4. Preserve rejected/deferred/paused options.
5. Write short roadmap and route forward.

## Context Budget

Always read:

- `00-control/current-state.md`
- `08-mvp-experiments/smallest-useful-experiment.md`

Read only if needed:

- `08-mvp-experiments/mvp-options.md`
- `08-mvp-experiments/experiment-design.md`
- `09-roadmap/*`

Do not read:

- execution files until roadmap exists
- future phase folders

Read `framework/rules/context-efficiency.md` only when unsure what to load.

## Ease Of Use Rules

- Ask only questions that block the next useful file update.
- Create only files needed for the current action.
- Keep outputs compact: bullets or tables, not long narrative.
- Preserve uncertainty labels and rejected alternatives.

## When To Use

Use for phase `09-decisions-roadmap`.

## Inputs

- MVP options
- Selected experiment
- Constraints

## Files To Read

- `00-control/current-state.md`
- selected experiment
- MVP options if needed

## Files To Write

- `09-roadmap/selected-path.md`
- `09-roadmap/rejected-options.md`
- `09-roadmap/roadmap.md`
- `00-control/decision-log.md`
- `00-control/current-state.md`
- `00-control/handoff.md` when Clean Handoff Mode is active

## Questions To Ask

- What path is selected?
- What is rejected, deferred, or paused?
- What milestones are needed?

## Blocking Conditions

- Selection criteria unclear.
- Rejected alternatives missing.
- Roadmap actions do not connect to experiment.

## Skip Behavior

Log risk that execution may start without owners or sequence.

## Outputs

- Selected path
- Preserved alternatives
- Short roadmap
- Decision log entries

## Quality Gate

Before marking this phase complete, apply `framework/rules/phase-quality-gates.md`. Do not complete the phase until required files, decisions, open questions, skip risks, evidence labels, rejected alternatives, current state, and handoff requirements are handled.

## Handoff Output

When Clean Handoff Mode is active, update `00-control/handoff.md` using `framework/rules/clean-handoff.md`. Include completed phase, files updated, confirmed decisions, key facts, key assumptions, open questions, skipped risks, recommended next skill, and minimum files the next skill must read.

## Next Recommended Skill

`idea-o-10-execution`
