---
name: problem-definition
description: Use when clarifying the user problem, beneficiary, current alternatives, and why the idea matters.
---

# Problem Definition

## Quick Start

1. Read current state and idea brief.
2. Create only `02-problem` files if missing.
3. Describe problem from user perspective.
4. Record current alternatives.
5. Update current state and route forward.

## Context Budget

Always read:

- `00-control/current-state.md`
- `01-idea/idea-brief.md`

Read only if needed:

- `02-problem/problem-context.md`
- `02-problem/user-context.md`
- `00-control/open-questions.md`

Do not read:

- research logs unless already summarized
- strategy files
- future phase folders

Read `framework/rules/context-efficiency.md` only when unsure what to load.

## Ease Of Use Rules

- Ask only questions that block the next useful file update.
- Create only files needed for the current action.
- Keep outputs compact: bullets or tables, not long narrative.
- Preserve uncertainty labels and rejected alternatives.

## When To Use

Use for phase `02-problem-context`.

## Inputs

- Idea brief
- Raw notes or import summary
- Known user context

## Files To Read

- `00-control/current-state.md`
- `01-idea/idea-brief.md`
- `01-idea/raw-notes.md` if needed

## Files To Write

- `02-problem/problem-context.md`
- `02-problem/user-context.md`
- `00-control/current-state.md`
- `00-control/open-questions.md`
- `00-control/handoff.md` when Clean Handoff Mode is active

## Questions To Ask

- Who has the problem?
- What do they do today?
- What makes it painful, costly, slow, risky, or important?

## Blocking Conditions

- No plausible user or beneficiary.
- Only a solution exists, not a problem.

## Skip Behavior

Log risk that strategy and MVP may target the wrong audience.

## Outputs

- Problem statement
- User context
- Current alternatives
- Open blockers

## Quality Gate

Before marking this phase complete, apply `framework/rules/phase-quality-gates.md`. Do not complete the phase until required files, decisions, open questions, skip risks, evidence labels, rejected alternatives, current state, and handoff requirements are handled.

## Handoff Output

When Clean Handoff Mode is active, update `00-control/handoff.md` using `framework/rules/clean-handoff.md`. Include completed phase, files updated, confirmed decisions, key facts, key assumptions, open questions, skipped risks, recommended next skill, and minimum files the next skill must read.

## Next Recommended Skill

`research-evidence`
