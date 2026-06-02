---
name: idea-o-00-import
description: Use when an idea project starts from existing material such as a long chat, document, transcript, research dump, strategy note, or mixed notes.
---

# Idea Import

## Quick Start

1. Receive or locate the source material.
2. Create only control files and `00-import` files if missing.
3. Choose an import fidelity mode: `Verbatim Preservation`, `Structured Faithful Summary`, or `Decision-Focused Summary`.
4. Preserve source or summarize according to the chosen mode.
5. Extract candidate ideas, classified claims, rejected alternatives, questions, and candidate decisions.
6. Ask the user to confirm main idea and decisions.

## Context Budget

Always read:

- Provided source material
- `00-control/current-state.md` if it exists
- `framework/rules/import-fidelity.md`

Read only if needed:

- `00-control/open-questions.md`
- `00-control/decision-log.md`

Do not read:

- future phase folders
- examples/
- templates/project/ unless creating import files

Resolve `framework/rules/...` from the project workspace first, then from the installed IDEA-O skill/framework location. Missing project-local rules are not a failure.

Read `framework/rules/context-efficiency.md` only when unsure what to load.

## Ease Of Use Rules

- Use `framework/rules/import-fidelity.md` to choose and record the fidelity mode, preservation choice, omissions, and remaining risk.
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

Use before normal intake when substantial existing material already exists.

## Inputs

- Chat, document, transcript, notes, or research dump
- Existing project files if any

## Files To Read

- Provided source material
- `00-control/current-state.md` if it exists

## Files To Write

- `00-control/current-state.md`
- `00-control/open-questions.md`
- `00-import/import-summary.md`
- `00-import/source-material.md` only when preserving source material locally or recording a source pointer there is useful
- `00-control/decision-log.md` for confirmed decisions only
- `00-control/handoff.md` when Clean Handoff Mode is active

## Questions To Ask

- Which fidelity mode should this import use: `Verbatim Preservation`, `Structured Faithful Summary`, or `Decision-Focused Summary`?
- Which candidate idea is the project focus?
- Are candidate decisions confirmed or still open?

## Blocking Conditions

- No source material.
- Several unrelated ideas with no chosen focus.
- Prior conclusions treated as confirmed decisions without user confirmation.

## Skip Behavior

If import is skipped, log risk of losing context, rejected alternatives, assumptions, or implied decisions.

## Outputs

- Preserved or summarized source
- Import summary
- Fidelity mode, preservation/omission notes, and remaining risk
- Candidate decisions separated from confirmed decisions
- Recommended next skill

## Quality Gate

Before marking this phase complete, apply `framework/rules/phase-quality-gates.md`. Do not complete the phase until required files, decisions, open questions, skip risks, evidence labels, rejected alternatives, current state, and handoff requirements are handled.

## Handoff Output

When Clean Handoff Mode is active, update `00-control/handoff.md` using `framework/rules/clean-handoff.md`. Include completed phase, files updated, confirmed decisions, key facts, key assumptions, open questions, skipped risks, recommended next skill, and minimum files the next skill must read.

## Next Recommended Skill

Primary `idea-o-01-intake`; use `idea-o-02-problem` when the main idea and user problem are already clear.
