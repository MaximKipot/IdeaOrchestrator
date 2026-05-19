---
name: idea-orchestrator
description: Use when starting, continuing, routing, skipping, jumping, or reviewing an idea project in the Codex idea framework; especially when the user uses plain-language commands like start, continue, run a phase, what next, skip this, or review.
---

# Idea Orchestrator

## Quick Start

Use this skill as the front door for the framework.

1. Read `00-control/current-state.md`. If it is missing, initialize the project from `templates/project/`.
2. Translate the user's plain-language request into one of: start, continue, run phase, skip, jump, review, or status.
3. Check blockers in `00-control/open-questions.md` before moving forward.
4. Run or recommend exactly one next phase skill unless the user asks for a broader review.
5. End by updating `00-control/current-state.md` with current phase, status, next action, and next recommended skill.

## Ease Of Use Rules

- Do not make the user learn the framework structure.
- Prefer a concrete proposed next step over an open-ended question.
- Ask only questions that block the next useful file update.
- If information is uncertain but not blocking, continue and label it as `Assumption` or `Guess`.
- Keep user-facing summaries short: current phase, next action, blockers, and files changed.
- Use the smallest useful phase step; do not expand into a full strategy session unless the user asks.

## Common User Commands

| User Says | Do This |
| --- | --- |
| Start a new idea | Initialize files, capture raw idea, recommend `idea-intake`. |
| Continue | Read current state, resolve blockers, run the next recommended skill. |
| What next? | Summarize current phase, blockers, and one recommended next action. |
| Run research | Route to `research-evidence` and check research depth. |
| Skip this | Log skipped item, risk, owner, and revisit trigger before advancing. |
| Jump to MVP | Allow the jump, log prior-phase risks, then route to `mvp-experiments`. |
| Review or pivot | Route to `review-pivot` and anchor the review in evidence. |

## Default Depth Selection

Suggest a depth, but let the user override it.

| Depth | Use When |
| --- | --- |
| `Light` | Personal, internal, low-risk, or exploratory idea. |
| `Standard` | Most software, business, service, workshop, content, or product ideas. |
| `Deep` | High-cost, high-risk, regulated, legal, financial, medical, safety-sensitive, or strategically important idea. |

If unsure, choose `Standard` and write the reason in `00-control/current-state.md`.

## When To Use

Use before any phase, when resuming a project, when interpreting a plain-language request, or when the user asks what to do next.

## Inputs

- User request
- Project files
- Desired depth override, if any
- Current blockers or skipped items

## Files To Read

- `AGENTS.md`
- `framework/rules/phase-transition-rules.md`
- `framework/rules/blocking-and-skipping.md`
- `00-control/current-state.md`
- `00-control/open-questions.md`
- `00-control/decision-log.md`

## Files To Write

- `00-control/current-state.md`
- `00-control/open-questions.md`
- `00-control/decision-log.md` when process decisions are made

## Questions To Ask

Ask at most one question at a time. Prefer these only when needed:

- Should I continue the next recommended phase or jump to a specific phase?
- Do you accept the logged risk of skipping this item?
- Should this use `Light`, `Standard`, or `Deep` depth?

## Blocking Conditions

- No project files exist and the user has not provided enough information to initialize them.
- `00-control/current-state.md` is missing and project setup is not being run.
- The requested jump would ignore an unresolved blocker without user acceptance.
- A required decision is being implied but not logged.

## Skip Behavior

If the user skips a phase, artifact, or question:

1. Log what was skipped.
2. Log why it was skipped.
3. Log the risk created.
4. Log who accepted the risk.
5. Log the revisit trigger.
6. Continue only after the skip is written to `00-control/current-state.md` or the relevant phase file.

## Outputs

- Current phase confirmed
- Depth confirmed or proposed
- Blockers identified
- One next action named
- Next recommended skill named
- Required control files updated

## Next Recommended Skill

Use the phase skill matching the current phase. If no phase is clear, use `idea-intake` for a new idea or `execution-tracking` for an active project with a selected path.
