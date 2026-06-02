---
name: idea-o-10-execution-rules
description: Use when an idea-o project will delegate implementation to AI agents and needs execution boundaries before work starts, especially for file permissions, verification, review checkpoints, stop conditions, or multi-agent work.
---

# Agent Execution Rules

## Quick Start

1. Read current state and implementation spec if it exists.
2. Create only `10-execution/agent-execution-rules.md` if missing.
3. Define execution boundaries, verification, checkpoints, and stop conditions.
4. Ask the user before choosing any execution-mode or permission fork.
5. Update control files and route to execution tracking.

## Context Budget

Always read:

- `00-control/current-state.md`
- `10-execution/implementation-spec.md` if present

Read only if needed:

- `09-roadmap/selected-path.md`
- `09-roadmap/roadmap.md`
- `10-execution/current-focus.md`
- `10-execution/next-actions.md`
- `00-control/open-questions.md`

Do not read:

- review files until reviewing
- unrelated future phase files
- implementation repositories unless rules need concrete file boundaries and the user has identified the repo

Resolve `framework/rules/...` from the project workspace first, then from the installed IDEA-O skill/framework location. Missing project-local rules are not a failure.

Read `framework/rules/context-efficiency.md` only when unsure what to load.

## Best-Practice Basis

- Agent rules should be short, explicit, and enforceable.
- Use guardrails and stop conditions for risky actions, not only positive guidance.
- Prefer concrete verification loops over trust-based completion.
- Split work across agents only when tasks are independent enough to avoid conflicting edits.
- Preserve handoff context: changed files, commands run, failures, unresolved forks, and evidence.
- Keep `00-control/current-state.md` as a compact dashboard with active decisions, blocking questions, recently changed files, and next action.
- Use decision lifecycle statuses in `00-control/decision-log.md`: Active, Superseded, Rejected, Deferred, Archived.
- Triage `00-control/open-questions.md` into Blocking Next Action, Decision Needed Soon, Research Later, Parking Lot, and Resolved.
- Include non-goals, forbidden assumptions, required verification evidence, and stop conditions that prevent agents from inventing scope.

## Decision Fork Rule

Ask the user before choosing:

- single-agent, checkpointed single-agent, sequential multi-agent, or parallel multi-agent execution
- whether agents may edit implementation files, framework files, tests, docs, generated assets, or configuration
- whether network access, dependency installation, destructive commands, migrations, deployments, or paid services are allowed
- review cadence, commit cadence, or PR strategy
- which verification commands are authoritative
- whether execution may proceed with open implementation-spec questions

If a fork is not blocking execution, log it in `00-control/open-questions.md` with owner, risk, and revisit trigger.

## Files To Write

- `10-execution/agent-execution-rules.md`
- `00-control/current-state.md`
- `00-control/open-questions.md` for unresolved forks
- `00-control/decision-log.md` for confirmed execution decisions
- `00-control/handoff.md` when Clean Handoff Mode is active

## Agent Execution Rules Contents

The rules should include:

- rules status, date, owner, and source files
- execution mode
- agent roles and responsibility boundaries
- allowed files and protected files
- non-goals and out-of-bounds work
- forbidden assumptions agents must not make
- tool and permission rules
- user-change preservation rules
- testing and verification commands
- review checkpoints
- stop conditions
- handoff requirements
- decision forks and open questions

Use evidence labels for claims that affect direction: `Fact`, `Assumption`, `Guess`, `Opinion`, `Preference`, `Decision`.

## Questions To Ask

- Who or what will execute the implementation?
- Should work run inline, checkpointed, sequentially across agents, or in parallel?
- What files or actions are off limits?
- What assumptions are forbidden without user confirmation?
- What commands or evidence prove the work is acceptable?
- When should agents stop and ask?

Ask one blocking question at a time.

## Blocking Conditions

- Implementation will be delegated, but file boundaries or permissions are unclear.
- Verification commands or acceptance evidence are missing.
- Multi-agent or parallel execution is possible, but task boundaries are not independent.
- Open implementation-spec questions would force agents to make unconfirmed decisions.

## Skip Behavior

If the user skips execution rules, log risk that agents may edit out-of-scope files, miss verification, overwrite user work, duplicate effort, or continue past a decision fork.

## Outputs

- Agent execution rules
- Confirmed execution decisions
- Logged open forks
- Next recommended skill

## Quality Gate

Before marking this prep complete, apply `framework/rules/phase-quality-gates.md`. Do not complete until required files, decisions, open questions, skip risks, evidence labels, rejected alternatives, current state, and handoff requirements are handled.

## Handoff Output

When Clean Handoff Mode is active, update `00-control/handoff.md` using `framework/rules/clean-handoff.md`. Include files updated, confirmed decisions, key facts, key assumptions, open forks, skipped risks, recommended next skill, and minimum files the next skill must read.

## Next Recommended Skill

Use `idea-o-10-execution`.
