---
name: idea-import
description: Use when an idea project starts from existing material such as a long chat, document, transcript, research dump, strategy note, or mixed notes.
---

# Idea Import

## Quick Start

1. Receive or locate the source material.
2. Create only control files and `00-import` files if missing.
3. Preserve source or a faithful summary.
4. Extract candidate ideas, classified claims, rejected alternatives, questions, and candidate decisions.
5. Ask the user to confirm main idea and decisions.

## Context Budget

Always read:

- Provided source material
- `00-control/current-state.md` if it exists

Read only if needed:

- `00-control/open-questions.md`
- `00-control/decision-log.md`

Do not read:

- future phase folders
- examples/
- templates/project/ unless creating import files

Read `framework/rules/context-efficiency.md` only when unsure what to load.

## Ease Of Use Rules

- Ask only questions that block the next useful file update.
- Create only files needed for the current action.
- Keep outputs compact: bullets or tables, not long narrative.
- Preserve uncertainty labels and rejected alternatives.

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
- `00-import/source-material.md`
- `00-import/import-summary.md`
- `00-control/decision-log.md` for confirmed decisions only
- `00-control/handoff.md` when Clean Handoff Mode is active

## Questions To Ask

- Preserve verbatim or summarize with reference?
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
- Candidate decisions separated from confirmed decisions
- Recommended next skill

## Quality Gate

Before marking this phase complete, apply `framework/rules/phase-quality-gates.md`. Do not complete the phase until required files, decisions, open questions, skip risks, evidence labels, rejected alternatives, current state, and handoff requirements are handled.

## Handoff Output

When Clean Handoff Mode is active, update `00-control/handoff.md` using `framework/rules/clean-handoff.md`. Include completed phase, files updated, confirmed decisions, key facts, key assumptions, open questions, skipped risks, recommended next skill, and minimum files the next skill must read.

## Next Recommended Skill

Primary `idea-intake`; use `problem-definition` when the main idea and user problem are already clear.
