---
name: idea-o-10-execution-evidence
description: Use when build, test, debug, launch, user feedback, or implementation work creates evidence that should update an idea project without forcing a full review phase.
---

# Execution Evidence Capture

## Quick Start

1. Read `00-control/current-state.md` and the relevant execution file.
2. Create or update only `10-execution/execution-evidence.md` when evidence needs detail.
3. Answer the capture questions in `framework/rules/execution-evidence-capture.md`.
4. Update `10-execution/progress-log.md`, current state, and decision log when relevant.
5. Route to `idea-o-11-review` only if evidence changes direction or requires broader review.

## Context Budget

Always read:

- `00-control/current-state.md`
- `10-execution/progress-log.md` if present

Read only if needed:

- `10-execution/current-focus.md`
- `10-execution/implementation-spec.md`
- `10-execution/execution-evidence.md`
- `00-control/decision-log.md` when a decision changed or is needed
- `00-control/open-questions.md` when evidence creates a blocker

Do not read:

- review files unless the evidence requires Phase 11
- future phase folders
- implementation repositories unless the user points to the execution result

Resolve `framework/rules/...` from the project workspace first, then from the installed IDEA-O skill/framework location. Missing project-local rules are not a failure.

## Files To Write

- `10-execution/execution-evidence.md` when evidence needs detail
- `10-execution/progress-log.md`
- `00-control/current-state.md`
- `00-control/decision-log.md` when a decision is confirmed, changed, superseded, rejected, or deferred
- `00-control/open-questions.md` when evidence creates a blocker
- relevant phase files when execution changes product, UX, research, risk, MVP, roadmap, or implementation-spec content
- `00-control/handoff.md` when Clean Handoff Mode is active

## Questions To Ask

- What new evidence did execution create?
- What produced it?
- Did a decision change or need confirmation?
- Was an assumption invalidated, weakened, or strengthened?
- Did user-visible behavior, scope, constraints, or success criteria change?
- Which files or control logs must be updated?

Ask one blocking question at a time.

## Blocking Conditions

- Evidence changes a decision, but the decision is not logged.
- Evidence invalidates a high-risk assumption, but no next validation or stop condition is recorded.
- Execution changed user-visible behavior without updating the relevant phase or implementation-spec file.

## Outputs

- Captured execution evidence
- Updated execution log
- Updated current state
- Decision-log or open-question updates when relevant
- Next recommended skill

## Next Recommended Skill

Use `idea-o-10-execution` for ordinary continuation. Use `idea-o-11-review` only when evidence changes direction, finishes an experiment, creates a pivot/stop/pause decision, or requires broader tradeoff review.
