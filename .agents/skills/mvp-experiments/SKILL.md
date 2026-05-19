---
name: mvp-experiments
description: Use when generating MVP options, designing experiments, or selecting the smallest useful next experiment.
---

# MVP Experiments

## Quick Start

1. Read `00-control/current-state.md`, assumptions, risks, target user, metrics, and constraints.
2. Create only this phase's required folders and files if they are missing; do not create later-phase folders.
3. Generate at least three MVP or experiment options.
4. Compare options by learning value, speed, cost, and risk.
5. Select the smallest useful experiment and preserve rejected options.
6. Log the decision, update `00-control/current-state.md`, and recommend `decision-roadmap`.

## Ease Of Use Rules

- Always look for a smaller experiment before selecting a larger one.
- Prefer experiments that test the riskiest assumption quickly.
- Do not let the first plausible idea become the only option.
- Keep rejected options visible so the user can revisit them later.

## When To Use

Use for phase `08-mvp-experiments`.

## Inputs

- Strategy
- Assumptions
- Risks
- Success metrics
- Constraints

## Files To Read

- `00-control/current-state.md`
- `04-assumptions-risks/assumptions.md`
- `04-assumptions-risks/risks.md`
- `07-strategy/target-user.md`
- `07-strategy/success-metrics.md`
- `06-principles/constraints.md`

## Files To Write

- `08-mvp-experiments/mvp-options.md`
- `08-mvp-experiments/smallest-useful-experiment.md`
- `08-mvp-experiments/experiment-design.md`
- `09-roadmap/rejected-options.md`
- `00-control/decision-log.md`
- `00-control/current-state.md`

## Questions To Ask

- What are at least three ways to test the idea?
- Which assumption does each option test?
- What is the smallest useful experiment?
- What options should be rejected or deferred?

## Blocking Conditions

- Only one option is considered.
- The selected experiment does not test an important assumption.
- Success criteria are missing.

## Skip Behavior

If alternatives are skipped, log the risk of prematurely committing to a weak experiment.

## Outputs

- Multiple MVP or experiment options
- Selected smallest useful experiment
- Experiment design
- Rejected options preserved

## Next Recommended Skill

`decision-roadmap`
