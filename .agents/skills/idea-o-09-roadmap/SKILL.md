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
5. Write short roadmap and route forward, using Phase 10 prep when implementation needs it.

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

Resolve `framework/rules/...` from the project workspace first, then from the installed IDEA-O skill/framework location. Missing project-local rules are not a failure.

Read `framework/rules/context-efficiency.md` only when unsure what to load.

## Ease Of Use Rules

- Ask only questions that block the next useful file update.
- Create only files needed for the current action.
- Keep outputs compact: bullets or tables, not long narrative.
- Preserve uncertainty labels and rejected alternatives.
- Keep `00-control/current-state.md` as a compact dashboard with active decisions, blocking questions, recently changed files, and next action; move long history elsewhere.
- Use decision lifecycle statuses in `00-control/decision-log.md`: Active, Superseded, Rejected, Deferred, Archived.
- Triage `00-control/open-questions.md` into Blocking Next Action, Decision Needed Soon, Research Later, Parking Lot, and Resolved.


## Persistence Rules

- Before writing, check `00-control/current-state.md`, unresolved `00-control/open-questions.md`, and existing phase files for what the user already completed, deliberately skipped, or left blocked.
- Treat a phase as unfinished until required outputs are written to files or consciously skipped with accepted risk.
- If required output is missing, keep going by updating the file, asking one blocking question, or logging a conscious skip.
- Do not mark the phase complete or recommend the next skill until outputs exist or each missing output has reason, risk, owner, date, and revisit trigger.
- If the user asks to skip or jump, state the risk briefly and record explicit acceptance before advancing.

## When To Use

Use for phase `09-decisions-roadmap`.

## Challenge Pass

Before finalizing the selected path, use `framework/rules/challenge-pass.md` to challenge why the path might be wrong, what rejected option may later prove better, and what stop/pivot trigger should be watched.

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
- Which decisions remain Active, and which are Superseded, Rejected, Deferred, or Archived?
- Does execution need an implementation spec before work starts?
- Will AI agents need explicit execution rules?

## Blocking Conditions

- Selection criteria unclear.
- Rejected alternatives missing.
- Roadmap actions do not connect to experiment.

## Skip Behavior

Log risk that execution may start without owners, sequence, implementation-ready requirements, or agent boundaries.

## Outputs

- Challenge findings for the selected path
- Selected path
- Preserved alternatives
- Short roadmap
- Decision log entries with lifecycle status and supersession links when decisions changed

## Quality Gate

Before marking this phase complete, apply `framework/rules/phase-quality-gates.md`. Do not complete the phase until required files, decisions, open questions, skip risks, evidence labels, rejected alternatives, current state, and handoff requirements are handled.

## Handoff Output

When Clean Handoff Mode is active, update `00-control/handoff.md` using `framework/rules/clean-handoff.md`. Include completed phase, files updated, confirmed decisions, key facts, key assumptions, open questions, skipped risks, recommended next skill, and minimum files the next skill must read.

## Next Recommended Skill

Use `idea-o-10-implementation-spec` when implementation-ready requirements, acceptance criteria, or verification are needed before execution. Use `idea-o-10-execution-rules` when AI agents need execution boundaries but the implementation spec is already sufficient. Otherwise use `idea-o-10-execution`.
