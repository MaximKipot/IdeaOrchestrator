---
name: decision-roadmap
description: Use when selecting the path, preserving rejected options, and turning an experiment into a practical roadmap.
---

# Decision Roadmap

## Quick Start

1. Read `00-control/current-state.md` and the MVP experiment files.
2. Create only this phase's required folders and files if they are missing; do not create later-phase folders.
3. Record the selected path.
4. Move rejected, deferred, or paused options into `09-roadmap/rejected-options.md`.
5. Create a short roadmap with owners, sequence, and status.
6. Log decisions, update `00-control/current-state.md`, and recommend `execution-tracking`.

## Ease Of Use Rules

- Keep the roadmap near-term and experiment-focused.
- Make the next action obvious.
- Preserve alternatives without relitigating them.
- Use owner, status, and revisit trigger fields to reduce follow-up questions.

## When To Use

Use for phase `09-decisions-roadmap`.

## Inputs

- MVP options
- Selected experiment
- Experiment design
- Constraints

## Files To Read

- `00-control/current-state.md`
- `08-mvp-experiments/mvp-options.md`
- `08-mvp-experiments/smallest-useful-experiment.md`
- `08-mvp-experiments/experiment-design.md`
- `09-roadmap/rejected-options.md`

## Files To Write

- `09-roadmap/selected-path.md`
- `09-roadmap/rejected-options.md`
- `09-roadmap/roadmap.md`
- `00-control/decision-log.md`
- `00-control/current-state.md`

## Questions To Ask

- What path is selected?
- What is rejected, deferred, or paused?
- What milestones are needed?
- What decision should be revisited after the experiment?

## Blocking Conditions

- Selection criteria are unclear.
- Rejected alternatives are missing.
- Roadmap actions do not connect to the selected experiment.

## Skip Behavior

If roadmap detail is skipped, log the risk that execution may start without owners or sequence.

## Outputs

- Selected path
- Roadmap
- Preserved rejected options
- Decision log entries

## Next Recommended Skill

`execution-tracking`
