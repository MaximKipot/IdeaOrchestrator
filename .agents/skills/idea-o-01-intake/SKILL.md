---
name: idea-o-01-intake
description: Use when capturing a fresh raw idea or sharpening an imported candidate idea into an initial idea brief.
---

# Idea Intake

## Quick Start

1. Read current state.
2. Create only `01-idea` files if missing.
3. Preserve raw notes.
4. Write a concise idea brief with evidence labels.
5. Update current state and route forward.

## Context Budget

Always read:

- `00-control/current-state.md`

Read only if needed:

- `00-import/import-summary.md` after import
- `01-idea/raw-notes.md`
- `01-idea/idea-brief.md`

Do not read:

- research files
- strategy files
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

Use for phase `01-idea-capture` or after `idea-o-00-import` needs main-idea sharpening.

## Inputs

- Raw idea
- Imported candidate idea
- Known preferences or constraints

## Files To Read

- `00-control/current-state.md`
- `00-import/import-summary.md` if imported
- `01-idea/raw-notes.md` if it exists

## Files To Write

- `01-idea/raw-notes.md`
- `01-idea/idea-brief.md`
- `00-control/current-state.md`
- `00-control/open-questions.md` if blocked
- `00-control/handoff.md` when Clean Handoff Mode is active

## Questions To Ask

- What is the idea?
- Who might it help?
- What outcome would make it worth exploring?

## Blocking Conditions

- No identifiable idea, audience, or desired outcome.

## Skip Behavior

If detailed intake is skipped, log risk that later phases may optimize around the wrong idea.

## Outputs

- Raw notes
- One-sentence idea
- Initial audience
- Desired outcome

## Quality Gate

Before marking this phase complete, apply `framework/rules/phase-quality-gates.md`. Do not complete the phase until required files, decisions, open questions, skip risks, evidence labels, rejected alternatives, current state, and handoff requirements are handled.

## Handoff Output

When Clean Handoff Mode is active, update `00-control/handoff.md` using `framework/rules/clean-handoff.md`. Include completed phase, files updated, confirmed decisions, key facts, key assumptions, open questions, skipped risks, recommended next skill, and minimum files the next skill must read.

## Next Recommended Skill

`idea-o-02-problem`
