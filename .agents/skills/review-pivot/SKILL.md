---
name: review-pivot
description: Use when reviewing experiment results, deciding whether to continue, adjust, pivot, pause, or stop an idea project.
---

# Review Pivot

## Quick Start

1. Read `00-control/current-state.md`, experiment design, success metrics, and progress log.
2. Summarize what changed and what was learned.
3. Decide whether to continue, adjust, pivot, pause, or stop.
4. Preserve abandoned paths and log pivot decisions.
5. Update `00-control/current-state.md` and recommend the next phase or action.

## Ease Of Use Rules

- Anchor review in evidence, not general sentiment.
- If evidence is thin, say so and choose the smallest next learning action.
- Do not erase the previous direction; preserve it as rejected, paused, or superseded.
- Keep the review decision plain and explicit.

## When To Use

Use for phase `11-review-pivot`, after an experiment, a milestone, a stall, or new contradictory evidence.

## Inputs

- Evidence map
- Experiment design
- Progress log
- Success metrics
- User judgment

## Files To Read

- `00-control/current-state.md`
- `03-research/evidence-map.md`
- `07-strategy/success-metrics.md`
- `08-mvp-experiments/experiment-design.md`
- `10-execution/progress-log.md`
- `11-review/review-log.md`

## Files To Write

- `11-review/review-log.md`
- `11-review/pivot-decisions.md`
- `09-roadmap/rejected-options.md`
- `00-control/decision-log.md`
- `00-control/current-state.md`

## Questions To Ask

- What did the evidence show?
- What changed since the last decision?
- Should the project continue, adjust, pivot, pause, or stop?
- What should be preserved for later?

## Blocking Conditions

- There is no evidence or progress to review.
- A pivot is proposed without naming consequences.

## Skip Behavior

If review is skipped, log the risk that the project may continue despite contradictory evidence.

## Outputs

- Review findings
- Continue, adjust, pivot, pause, or stop decision
- Preserved alternatives
- Updated current state

## Next Recommended Skill

`idea-orchestrator` to choose the next phase or continue execution.

