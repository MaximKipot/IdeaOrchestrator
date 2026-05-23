---
name: idea-o-03-research
description: Use when gathering, classifying, or summarizing evidence for an idea project.
---

# Research Evidence

## Quick Start

1. Read current state, idea brief, and problem context.
2. Create only `03-research` files if missing.
3. Pick Light, Standard, or Deep depth.
4. Choose research mode: Founder Assumption Audit, End-User Questionnaire, or Mixed.
5. Always run a market scan for present solutions and alternatives.
6. Log sources and classify evidence.
7. Update current state and route forward.

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

## Research Mode Fork

Choose one mode before detailed research. The user may override it.

| Mode | Use When | Output |
| --- | --- | --- |
| `Founder Assumption Audit` | The idea is early, founder-led, or based mostly on internal belief. | A ranked list of founder assumptions, what would validate or falsify each, and the smallest evidence step. |
| `End-User Questionnaire` | The target user or buyer can be reached and user evidence is needed. | Interview or survey questions tied to assumptions, with what each question is meant to reveal. |
| `Mixed` | Most product, service, business, or market-facing ideas. | Both assumption audit and questionnaire, kept short enough to act on. |

Every mode must include a market scan for present solutions, substitutes, current workarounds, and comparable alternatives.

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
- Which research mode should be used: Founder Assumption Audit, End-User Questionnaire, or Mixed?
- Any specific sources, competitors, users, or markets?

## Blocking Conditions

- No research can be logged.
- Claims are treated as facts without sources.
- Present solutions or substitutes have not been checked.
- High-risk domains lack explicit uncertainty.

## Skip Behavior

Research may be narrowed, not removed; log deferred research and risk.

## Outputs

- Research log
- Source list
- Evidence map
- Founder assumptions and validation tests when that mode is used
- End-user questionnaire when that mode is used
- Market scan for present solutions in every mode
- Research gaps

## Quality Gate

Before marking this phase complete, apply `framework/rules/phase-quality-gates.md`. Do not complete the phase until required files, decisions, open questions, skip risks, evidence labels, rejected alternatives, current state, and handoff requirements are handled.

## Handoff Output

When Clean Handoff Mode is active, update `00-control/handoff.md` using `framework/rules/clean-handoff.md`. Include completed phase, files updated, confirmed decisions, key facts, key assumptions, open questions, skipped risks, recommended next skill, and minimum files the next skill must read.

## Next Recommended Skill

`idea-o-04-risks`
