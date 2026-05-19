---
name: mvp-experiments
description: Use when generating MVP options, designing experiments, or selecting the smallest useful next experiment.
---

# MVP Experiments

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

