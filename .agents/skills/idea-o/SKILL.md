---
name: idea-o
description: Use when routing, starting, continuing, importing, skipping, jumping, reviewing, or answering what to do next in an idea project.
---

# Idea Orchestrator

## Quick Start

1. Read `00-control/current-state.md`; create only control files if missing.
2. Use `framework/index.md` when routing is unclear.
3. Route to one skill: import, intake, phase, execution, or review.
4. Log jumps, skips, blockers, and process decisions.
5. Update current state with next action and next recommended skill.

## Context Budget

Always read:

- `00-control/current-state.md`

Read only if needed:

- `framework/index.md` for routing
- `00-control/open-questions.md` for blockers
- `00-control/decision-log.md` for decisions

Do not read:

- examples/
- templates/project/ unless creating a file
- future phase folders

Read `framework/rules/context-efficiency.md` only when unsure what to load.

## Ease Of Use Rules

- Ask only questions that block the next useful file update.
- Create only files needed for the current action.
- Keep outputs compact: bullets or tables, not long narrative.
- Preserve uncertainty labels and rejected alternatives.

## When To Use

Use as the front door whenever the user gives a plain-language process request.

## Inputs

- User request
- Existing project state
- Optional depth preference

## Files To Read

- `00-control/current-state.md`
- `framework/index.md` when route is unclear
- `00-control/open-questions.md` when blocked or skipped

## Files To Write

- `00-control/current-state.md`
- `00-control/open-questions.md` for blockers/skips
- `00-control/decision-log.md` for process decisions
- `00-control/handoff.md` when Clean Handoff Mode is active

## Questions To Ask

- Which project focus should I use?
- Do you accept the logged risk of skipping or jumping?
- Should depth be Light, Standard, or Deep?

## Blocking Conditions

- No project folder or usable starting material.
- A jump or skip risk is not accepted.
- A decision is implied but not logged.

## Skip Behavior

Log skipped item, reason, risk, owner, date, and revisit trigger before advancing.

## Outputs

- Current phase
- Next action
- Next recommended skill
- Any blockers or skip risks

## Quality Gate

Before marking this phase complete, apply `framework/rules/phase-quality-gates.md`. Do not complete the phase until required files, decisions, open questions, skip risks, evidence labels, rejected alternatives, current state, and handoff requirements are handled.

## Handoff Output

When Clean Handoff Mode is active, update `00-control/handoff.md` using `framework/rules/clean-handoff.md`. Include completed phase, files updated, confirmed decisions, key facts, key assumptions, open questions, skipped risks, recommended next skill, and minimum files the next skill must read.

## Next Recommended Skill

Use the routed skill. If existing material is provided, use `idea-o-import`; if fresh, use `idea-o-intake`.
