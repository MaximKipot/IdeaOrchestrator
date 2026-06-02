# Phase Transition Rules

The normal process is sequential:

Optional pre-initial import: existing material import
0. Project setup
1. Idea capture
2. Problem context
3. Research evidence
4. Assumptions and risks
5. Vision and direction
6. Principles and constraints
7. Strategy
8. MVP and experiments
9. Decisions and roadmap
Optional Phase 10 prep after roadmap:
- `idea-o-10-implementation-spec` when implementation-ready requirements, acceptance criteria, non-goals, forbidden assumptions, or verification expectations are needed.
- `idea-o-10-execution-rules` when AI agents need file boundaries, permissions, execution mode, stop conditions, or verification rules.
10. Execution tracking
Optional Phase 10 evidence capture:
- `idea-o-10-execution-evidence` when build, test, debug, launch, user feedback, or implementation work creates evidence that should update project memory without a full review phase.
11. Review and pivot
Utility route:
- `idea-o-publish` when idea artifacts need branch, stage, commit, push, or PR safety.

Execution must not start when agents would need to invent requirements, permissions, execution mode, or verification rules. Route through `idea-o-10-implementation-spec` and/or `idea-o-10-execution-rules`, or log an explicit user-accepted skip risk before execution begins.

## Transition Requirements

Before starting a phase:

- Read `00-control/current-state.md`.
- Read unresolved items in `00-control/open-questions.md`.
- Check what the user already completed, deliberately skipped, or left blocked.
- Confirm the phase is not blocked.
- Use the relevant skill.
- Create only the folders and files needed for the phase being started.
- Do not create future phase folders in advance.

## Import Transition

Use `idea-o-00-import` before phase 1 when the user provides substantial existing material.

Import is complete when:

- The source material is preserved or summarized according to the chosen fidelity mode.
- `00-import/import-summary.md` records the chosen fidelity mode, rationale, what was preserved, what was omitted, remaining risk, and any source pointer needed when exact wording may matter.
- Candidate ideas and claims are classified.
- Candidate decisions are separated from confirmed decisions.
- The user has a recommended next normal phase.

After import, route to `idea-o-01-intake` when the main idea still needs confirmation, or `idea-o-02-problem` when the main idea is already clear.

Before leaving a phase:

- Update the phase output files.
- Log decisions.
- Log skipped items and risks.
- Do not advance until outputs are written or skipped with explicit accepted risk.
- Apply `framework/rules/phase-quality-gates.md`.
- Update `00-control/current-state.md`.
- Recommend the next phase.

## Phase 09 To Phase 10 Prep

After `idea-o-09-roadmap`, choose the next skill explicitly:

- Use `idea-o-10-implementation-spec` when the selected path is concrete implementation work and requirements, acceptance criteria, non-goals, forbidden assumptions, or verification expectations are not implementation-ready.
- Use `idea-o-10-execution-rules` when AI agents will execute the work and boundaries, permissions, execution mode, stop conditions, or verification rules are unclear.
- Use `idea-o-10-execution` only when implementation requirements and execution boundaries are already clear enough that agents will not need to invent them.

If the user skips either prep step, record the skipped item, reason, risk, owner, date, and revisit trigger before starting execution tracking.

## Phase 10 Evidence Capture

Use `idea-o-10-execution-evidence` when execution teaches the idea something durable but the project does not need Phase 11 yet. Return to `idea-o-10-execution` after updating `10-execution`, `00-control/current-state.md`, and `00-control/decision-log.md` when relevant.

Move to `idea-o-11-review` when execution evidence changes direction, finishes an experiment, creates a pivot/stop/pause decision, or requires broader tradeoff review.

## Publish Utility

Use `idea-o-publish` for idea artifact publishing requests. Confirm target folder, base branch, branch name, staging scope, and wrong-folder checks before any git write, then record the publish decision in control files.

## Manual Jumps

Manual jumping is allowed only when requested by the user.

When jumping:

- Record the requested jump.
- Record unresolved prior-phase risks.
- Continue with the requested phase.
- Create only the requested phase's needed files.
- Recommend revisiting skipped phases when relevant.
