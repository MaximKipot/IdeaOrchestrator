---
name: idea-o-10-implementation-spec
description: Use when an idea-o project needs an implementation-ready specification before execution, especially for AI agent delegation, software build work, concrete experiments, or unclear acceptance criteria.
---

# Implementation Spec

## Quick Start

1. Read current state, selected path, roadmap, and experiment design.
2. Create only `10-execution/implementation-spec.md` if missing.
3. Translate the selected path into build-ready requirements.
4. Ask the user before resolving any meaningful decision fork.
5. Update control files and route to execution rules or execution tracking.

## Context Budget

Always read:

- `00-control/current-state.md`
- `09-roadmap/selected-path.md`
- `09-roadmap/roadmap.md`

Read only if needed:

- `08-mvp-experiments/experiment-design.md`
- `07-strategy/success-metrics.md`
- `06-principles/constraints.md`
- `10-execution/implementation-spec.md`
- `00-control/open-questions.md`

Do not read:

- full source material after it has been summarized
- unrelated future phase files
- implementation repositories unless the roadmap names them or the user points to them

Resolve `framework/rules/...` from the project workspace first, then from the installed IDEA-O skill/framework location. Missing project-local rules are not a failure.

Read `framework/rules/context-efficiency.md` only when unsure what to load.

## Best-Practice Basis

- Keep instructions specific, structured, and separated from context.
- Define objective, scope, non-goals, forbidden assumptions, acceptance criteria, and verification evidence.
- Prefer concrete checks, commands, examples, and expected outputs over broad guidance.
- Keep agent-facing specs concise enough to be followed.
- Record unresolved forks instead of letting implementation agents invent product, architecture, cost, safety, or verification decisions.
- Keep `00-control/current-state.md` as a compact dashboard with active decisions, blocking questions, recently changed files, and next action.
- Use decision lifecycle statuses in `00-control/decision-log.md`: Active, Superseded, Rejected, Deferred, Archived.
- Triage `00-control/open-questions.md` into Blocking Next Action, Decision Needed Soon, Research Later, Parking Lot, and Resolved.
- Include a Spec Kit compatible prompt section when the spec will be handed to Spec Kit or another implementation planner.

## Decision Fork Rule

Ask the user before choosing any fork that changes:

- user-visible behavior
- target user, use case, or success definition
- scope, non-goals, or acceptance criteria
- technical architecture, framework, data model, API, persistence, auth, payments, or third-party services
- cost, privacy, security, legal, safety, or operational risk
- verification standard, launch gate, or rollback expectation
- whether a deferred/rejected option becomes active again

If the fork is not blocking execution, log it in `00-control/open-questions.md` with owner, risk, and revisit trigger.

## Files To Write

- `10-execution/implementation-spec.md`
- `00-control/current-state.md`
- `00-control/open-questions.md` for unresolved forks
- `00-control/decision-log.md` for confirmed implementation decisions
- `00-control/handoff.md` when Clean Handoff Mode is active

## Implementation Spec Contents

The spec should include:

- spec status, date, owner, and source files
- objective and user outcome
- in scope and out of scope
- non-goals and forbidden assumptions
- functional requirements
- constraints and dependencies
- interface, data, or system notes when relevant
- acceptance criteria
- verification plan with commands or observable evidence
- Spec Kit compatible prompt output when useful
- decision forks and open questions
- handoff notes for execution agents

Use evidence labels for claims that affect direction: `Fact`, `Assumption`, `Guess`, `Opinion`, `Preference`, `Decision`.

## Questions To Ask

- What exactly should the implementation produce?
- What must be excluded?
- What assumptions are forbidden for implementation agents to make?
- What behavior or outcome proves this is done?
- What verification evidence is acceptable?
- Which decision fork should be resolved before execution?

Ask one blocking question at a time.

## Blocking Conditions

- No selected path or roadmap exists.
- Scope or acceptance criteria are ambiguous enough that an implementation agent would need to invent requirements.
- A technical, product, cost, privacy, safety, or verification decision is required before work can start.

## Skip Behavior

If the user skips the implementation spec, log risk that execution agents may build the wrong thing, overbuild, under-test, or make unconfirmed decisions.

## Outputs

- Implementation-ready spec
- Confirmed implementation decisions
- Logged open forks
- Next recommended skill

## Quality Gate

Before marking this prep complete, apply `framework/rules/phase-quality-gates.md`. Do not complete until required files, decisions, open questions, skip risks, evidence labels, rejected alternatives, current state, and handoff requirements are handled.

## Handoff Output

When Clean Handoff Mode is active, update `00-control/handoff.md` using `framework/rules/clean-handoff.md`. Include files updated, confirmed decisions, key facts, key assumptions, open forks, skipped risks, recommended next skill, and minimum files the next skill must read.

## Next Recommended Skill

Use `idea-o-10-execution-rules` when AI agents will implement the work or execution boundaries matter. Otherwise use `idea-o-10-execution`.
