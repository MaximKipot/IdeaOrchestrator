---
name: idea-o-10-execution
description: Use when tracking current focus, next actions, progress, blockers, or evidence from execution.
---

# Execution Tracking

## Quick Start

1. Read current state and selected path.
2. Create only `10-execution` files if missing.
3. Update current focus.
4. Record next actions and progress.
5. Recommend review when evidence exists.

## Context Budget

Always read:

- `00-control/current-state.md`
- `09-roadmap/selected-path.md`

Read only if needed:

- `09-roadmap/roadmap.md`
- `10-execution/*`
- `00-control/open-questions.md` for blockers

Do not read:

- review files until reviewing
- future phase folders

Read `framework/rules/context-efficiency.md` only when unsure what to load.

## Ease Of Use Rules

- Ask only questions that block the next useful file update.
- Create only files needed for the current action.
- Keep outputs compact: bullets or tables, not long narrative.
- Preserve uncertainty labels and rejected alternatives.


## Persistence Rules

- Before writing, check `00-control/current-state.md`, unresolved `00-control/open-questions.md`, and existing phase files for what the user already completed, deliberately skipped, or left blocked.
- Treat a phase as unfinished until required outputs are written to files or consciously skipped with accepted risk.
- If required output is missing, keep going by updating the file, asking one blocking question, or logging a conscious skip.
- Do not mark the phase complete or recommend the next skill until outputs exist or each missing output has reason, risk, owner, date, and revisit trigger.
- If the user asks to skip or jump, state the risk briefly and record explicit acceptance before advancing.

## When To Use

Use for phase `10-execution-tracking`.

## Inputs

- Selected path
- Roadmap
- Current progress
- New evidence or blockers

## Files To Read

- `00-control/current-state.md`
- selected path
- roadmap/current execution files if present

## Files To Write

- `10-execution/current-focus.md`
- `10-execution/next-actions.md`
- `10-execution/progress-log.md`
- `00-control/current-state.md`
- `00-control/open-questions.md`
- `00-control/decision-log.md` if execution creates a decision
- `00-control/handoff.md` when Clean Handoff Mode is active

## Questions To Ask

- What changed?
- What is the current focus?
- What is the next action?
- Is anything blocked?

## Blocking Conditions

- No owner or next action.
- New evidence requires a decision before continuing.

## Skip Behavior

Log risk that future reviews will lack evidence.

## Outputs

- Current focus
- Next actions
- Progress log
- Blockers or decisions

## Quality Gate

Before marking this phase complete, apply `framework/rules/phase-quality-gates.md`. Do not complete the phase until required files, decisions, open questions, skip risks, evidence labels, rejected alternatives, current state, and handoff requirements are handled.

## Handoff Output

When Clean Handoff Mode is active, update `00-control/handoff.md` using `framework/rules/clean-handoff.md`. Include completed phase, files updated, confirmed decisions, key facts, key assumptions, open questions, skipped risks, recommended next skill, and minimum files the next skill must read.

## Next Recommended Skill

`idea-o-11-review` when enough evidence exists; otherwise continue `idea-o-10-execution`.
