---
name: research-evidence
description: Use when gathering, classifying, or summarizing evidence for an idea project.
---

# Research Evidence

## Quick Start

1. Read current state, idea brief, and problem context.
2. Create only `03-research` files if missing.
3. Pick Light, Standard, or Deep depth.
4. Log sources and classify evidence.
5. Update current state and route forward.

## Context Budget

Always read:

- `00-control/current-state.md`
- `01-idea/idea-brief.md`
- `02-problem/problem-context.md`

Read only if needed:

- `03-research/research-log.md`
- `03-research/evidence-map.md`
- `03-research/source-list.md`

Do not read:

- examples/
- future phase folders
- full source dumps after summarized

Read `framework/rules/context-efficiency.md` only when unsure what to load.

## Ease Of Use Rules

- Ask only questions that block the next useful file update.
- Create only files needed for the current action.
- Keep outputs compact: bullets or tables, not long narrative.
- Preserve uncertainty labels and rejected alternatives.

## When To Use

Use for phase `03-research-evidence`.

## Inputs

- Idea brief
- Problem context
- Research questions
- Sources or notes

## Files To Read

- `00-control/current-state.md`
- `01-idea/idea-brief.md`
- `02-problem/problem-context.md`
- existing `03-research` files if present

## Files To Write

- `03-research/research-log.md`
- `03-research/evidence-map.md`
- `03-research/source-list.md`
- `00-control/current-state.md`
- `00-control/open-questions.md`
- `00-control/handoff.md` when Clean Handoff Mode is active

## Questions To Ask

- What must be true?
- What depth is appropriate?
- Any specific sources, competitors, users, or markets?

## Blocking Conditions

- No research can be logged.
- Claims are treated as facts without sources.
- High-risk domains lack explicit uncertainty.

## Skip Behavior

Research may be narrowed, not removed; log deferred research and risk.

## Outputs

- Research log
- Source list
- Evidence map
- Research gaps

## Handoff Output

When Clean Handoff Mode is active, update `00-control/handoff.md` using `framework/rules/clean-handoff.md`. Include completed phase, files updated, confirmed decisions, key facts, key assumptions, open questions, skipped risks, recommended next skill, and minimum files the next skill must read.

## Next Recommended Skill

`assumptions-risks`
