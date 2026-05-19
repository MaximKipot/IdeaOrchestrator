---
name: execution-tracking
description: Use when tracking progress, current focus, next actions, and evidence produced during execution.
---

# Execution Tracking

## When To Use

Use for phase `10-execution-tracking`.

## Inputs

- Selected path
- Roadmap
- Current progress
- New evidence or blockers

## Files To Read

- `00-control/current-state.md`
- `09-roadmap/selected-path.md`
- `09-roadmap/roadmap.md`
- `10-execution/next-actions.md`
- `10-execution/progress-log.md`
- `10-execution/current-focus.md`

## Files To Write

- `10-execution/next-actions.md`
- `10-execution/progress-log.md`
- `10-execution/current-focus.md`
- `00-control/open-questions.md`
- `00-control/current-state.md`
- `00-control/decision-log.md` when execution produces a decision

## Questions To Ask

- What changed since the last update?
- What is the current focus?
- What is the next action?
- What evidence did execution create?
- Is anything blocked?

## Blocking Conditions

- No owner or next action exists.
- New evidence requires a decision before continuing.

## Skip Behavior

If progress logging is skipped, log the risk that future reviews will lack evidence.

## Outputs

- Current focus
- Next actions
- Progress log
- Blockers or decisions surfaced

## Next Recommended Skill

`review-pivot` when enough evidence exists; otherwise continue `execution-tracking`.

