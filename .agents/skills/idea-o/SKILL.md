---
name: idea-o
description: Use when routing, starting, continuing, importing, skipping, jumping, reviewing, or answering what to do next in an idea project.
---

# Idea Orchestrator

## Quick Start

1. Read `00-control/current-state.md`; create only control files if missing.
2. Use `framework/index.md` when routing is unclear.
3. For direct reasoning, process, or product questions, answer first and update files only if durable project memory changes.
4. Route to one skill only when the request needs import, intake, phase, Phase 10 prep, execution evidence, publish, or review.
5. Log jumps, skips, blockers, and process decisions.
6. Update current state with next action and next recommended skill when a file update is needed.

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

Resolve `framework/rules/...` from the project workspace first, then from the installed IDEA-O skill/framework location. Missing project-local rules are not a failure.

Read `framework/rules/context-efficiency.md` only when unsure what to load.

## Ease Of Use Rules

- Direct questions are allowed inside idea projects. Answer the question first, then decide whether the answer changes durable project memory.
- Update Markdown only when the answer changes a decision, risk, evidence item, assumption, open question, rejected alternative, artifact index, current focus, or next action. If not, say no file update was required.
- Ask only questions that block the next useful file update.
- Create only files needed for the current action.
- Keep outputs compact: bullets or tables, not long narrative.
- Preserve uncertainty labels and rejected alternatives.
- Keep `00-control/current-state.md` as a compact dashboard with active decisions, blocking questions, recently changed files, and next action; move long history elsewhere.
- Use decision lifecycle statuses in `00-control/decision-log.md`: Active, Superseded, Rejected, Deferred, Archived.
- Triage `00-control/open-questions.md` into Blocking Next Action, Decision Needed Soon, Research Later, Parking Lot, and Resolved.
- Index custom or optional UX artifacts in `00-control/current-state.md` with purpose, status, owner, and next use.
- For child idea tracks, create only control files and `00-control/track-context.md`; use `framework/rules/sub-idea-tracks.md`.


## Persistence Rules

- Before writing, check `00-control/current-state.md`, unresolved `00-control/open-questions.md`, and existing phase files for what the user already completed, deliberately skipped, or left blocked.
- Treat a phase as unfinished until required outputs are written to files or consciously skipped with accepted risk.
- If required output is missing, keep going by updating the file, asking one blocking question, or logging a conscious skip.
- Do not mark the phase complete or recommend the next skill until outputs exist or each missing output has reason, risk, owner, date, and revisit trigger.
- If the user asks to skip or jump, state the risk briefly and record explicit acceptance before advancing.

## When To Use

Use as the front door whenever the user gives a plain-language process request.

Also use it for direct reasoning, process, or product questions inside an idea project. These do not require a phase run by default: answer first, make the smallest relevant durable update when needed, and route to a phase only when the user asks or actual phase outputs are needed.

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
- Does execution need an implementation spec or agent execution rules before work starts?
- Is this a sub-idea track that needs parent context and promotion rules?
- Is this a publish request that needs target folder, base branch, branch name, and staging scope confirmed?

## Blocking Conditions

- No project folder or usable starting material.
- A jump or skip risk is not accepted.
- A decision is implied but not logged.
- A publish or sub-track request lacks enough folder or parent context to prevent wrong-folder work.

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

Use the routed skill. If existing material is provided, use `idea-o-00-import`; if fresh, use `idea-o-01-intake`. Use `idea-o-publish` for branch, staging, commit, push, or PR requests involving idea artifacts. After roadmap, use `idea-o-10-implementation-spec` or `idea-o-10-execution-rules` before `idea-o-10-execution` when implementation requirements or agent boundaries need to be explicit. Use `idea-o-10-execution-evidence` when execution creates evidence worth preserving without a full review.
