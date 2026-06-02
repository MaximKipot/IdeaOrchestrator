# Codex Idea Development Framework

A reusable Markdown-first framework for turning raw business or actionable ideas into researched directions, principles, strategy, MVP or experiment options, decisions, next actions, and review loops.

The framework is built for Codex. It keeps the project memory in files so work can continue across sessions without depending on chat history.

It is also context-efficient by default: Codex should read the current state first, then only the files needed for the current phase.

It is persistence-oriented: each skill should help finish written outputs, identify what is already done, and distinguish conscious skips from unresolved gaps.

It also supports direct reasoning inside projects: Codex should answer direct process, product, or reasoning questions first, then update Markdown only when durable project memory changes.

It also includes a lightweight challenge pass: research, risks, MVP, roadmap, and review phases should deliberately ask what could make the idea fail before advancing.

Framework rule lookup is project-local first, then installed-skill or framework-relative. A missing project-local `framework/rules/...` file is not a failure if the installed IDEA-O copy is available.

## Skill Sequence

Use `idea-o` as the router. The numbered skills show the normal order in slash search:

| Order | Skill | Purpose |
| --- | --- | --- |
| Optional | `idea-o-00-import` | Import an existing chat, document, transcript, or notes dump. |
| 01 | `idea-o-01-intake` | Capture or sharpen the raw idea. |
| 02 | `idea-o-02-problem` | Define problem, user, context, and current alternatives. |
| 03 | `idea-o-03-research` | Gather and classify evidence, with a founder-assumption, end-user-questionnaire, or mixed research mode. |
| 04 | `idea-o-04-risks` | Sort assumptions, risks, unknowns, and tests. |
| 05 | `idea-o-05-vision` | Define vision, direction, and anti-vision. |
| 06 | `idea-o-06-principles` | Set principles, constraints, and tradeoff rules. |
| 07 | `idea-o-07-strategy` | Define target, value, positioning, model, distribution, and metrics. |
| 08 | `idea-o-08-mvp` | Generate MVP and experiment options. |
| 09 | `idea-o-09-roadmap` | Select a path, preserve rejected options, and plan the roadmap. |
| 10 prep | `idea-o-10-implementation-spec` | Create implementation-ready requirements, acceptance criteria, and verification. |
| 10 prep | `idea-o-10-execution-rules` | Define AI agent execution boundaries, checkpoints, stop conditions, and handoff rules. |
| 10 | `idea-o-10-execution` | Track focus, progress, blockers, and next actions. |
| 10 | `idea-o-10-execution-evidence` | Capture build, test, debug, launch, feedback, or implementation evidence without forcing full review. |
| 11 | `idea-o-11-review` | Review evidence and decide whether to continue, adjust, pivot, pause, or stop. |
| Utility | `idea-o-publish` | Safely branch, stage, commit, push, or open a PR for idea artifacts. |

Phase 10 prep is optional but explicit:

`idea-o-09-roadmap` -> `idea-o-10-implementation-spec` -> `idea-o-10-execution-rules` -> `idea-o-10-execution`

Use it when the roadmap has become concrete implementation work, especially if AI agents will execute the build. The implementation spec and execution rules live as sibling files in `10-execution/`.

The implementation spec should include non-goals, forbidden assumptions, acceptance criteria, verification expectations, and a Spec Kit compatible prompt when the work will move into Spec Kit. Agent execution rules should define allowed files, protected files/actions, verification commands, stop conditions, and handoff evidence.

Phase 10 can also capture execution evidence without requiring a full review:

`idea-o-10-execution` -> `idea-o-10-execution-evidence` -> `idea-o-10-execution`

Use this when build, test, debug, launch, user feedback, or implementation work changes evidence, assumptions, user-visible behavior, or decisions. Move to `idea-o-11-review` only when the evidence changes direction, finishes an experiment, creates a pivot/stop/pause decision, or needs broader tradeoff review.

## When To Use It

Use this framework for software ideas, businesses, services, internal initiatives, workshops, content projects, physical products, or personal projects.

It works best when an idea is still uncertain and needs structured development before execution.

## Start A New Idea Project

1. Create only one empty project folder for the idea.
2. Open that folder with Codex.
3. Ask Codex to use `.agents/skills/idea-o/SKILL.md`.
4. Codex creates only the control files needed to start:
   - `00-control/current-state.md`
   - `00-control/open-questions.md`
   - `00-control/decision-log.md`
5. Codex creates phase folders and files only when that phase starts or when a file is actually needed.
6. Let Codex suggest a depth level, then accept or override it.

Do not copy `templates/project/` into the new project. The templates are reference patterns, not an up-front scaffold.

Suggested depth levels:

- `Light`: personal, internal, or low-risk idea.
- `Standard`: most business, software, service, or content ideas.
- `Deep`: high-cost, high-risk, regulated, or strategically important idea.
- `Assumption-led`: fast mode for high-risk assumptions and decision-relevant research. It narrows research but still requires a market scan, evidence labels, deferred research risk, and the smallest validation step.

## Start From Existing Material

Use `idea-o-00-import` before normal intake when you already have a long chat, document, transcript, research dump, strategy note, or mixed notes.

Ask Codex:

> Import this existing material and turn it into an idea project.

Codex should:

1. Create the control files if they do not exist.
2. Choose and record an import fidelity mode: `Verbatim Preservation`, `Structured Faithful Summary`, or `Decision-Focused Summary`.
3. Create only the import files needed for the chosen fidelity mode:
   - `00-import/import-summary.md`
   - `00-import/source-material.md` only when preserving source material locally or recording a source pointer there is useful
4. Preserve the original material, a source pointer, or a summary according to the fidelity mode.
5. Record why the mode was chosen, what was preserved, what was omitted, remaining risk, and a source pointer when exact wording may matter.
6. Extract candidate ideas, facts, assumptions, guesses, opinions, preferences, rejected alternatives, open questions, and candidate decisions.
7. Ask you to confirm the main idea and any candidate decisions.
8. Route into `idea-o-01-intake` or `idea-o-02-problem`.

Old chat conclusions are not automatically decisions. They become decisions only after you confirm them.

Imports do not need to preserve huge verbatim transcripts by default. The fidelity mode makes compression explicit and logs the risk.

## Continue An Existing Idea Project

Ask Codex to:

1. Read `00-control/current-state.md`.
2. Read `00-control/open-questions.md` only when blocked, skipped, or unclear.
3. Identify what is already completed, deliberately skipped, or still blocked.
4. Continue the next recommended phase unless you request a manual jump.

Codex should not read examples, templates, future phase folders, or every rule file unless the current task needs them.

For direct questions, Codex should answer first and only make the smallest relevant file update when the answer changes a decision, risk, evidence item, assumption, open question, rejected alternative, artifact index, current focus, or next action. If no durable update is needed, Codex should say no file update was required.

`00-control/current-state.md` should stay a compact dashboard: current phase/status, current focus, active decisions, blocking questions, recently changed files, next recommended skill, and next action. Move long history into phase files or `00-control/project-history.md` only when needed.

`00-control/decision-log.md` should keep an active-decision summary near the top and mark each decision as Active, Superseded, Rejected, Deferred, or Archived. Superseded decisions link to their replacements.

`00-control/open-questions.md` should be triaged into Blocking Next Action, Decision Needed Soon, Research Later, Parking Lot, and Resolved, with owner, phase/status, and revisit trigger.

Optional UX and custom artifacts should be indexed in `00-control/current-state.md` with file, purpose, status, owner, and next use. This keeps files like `screen-map.md`, `copy-decisions.md`, `interaction-rules.md`, `permission-experience.md`, or other custom phase-local notes discoverable without creating a rigid new track.

## Sub-Idea Tracks

Use a sub-idea track when a focused child question needs its own idea files but should stay connected to a parent project.

Create only the child project folder, control files, and `00-control/track-context.md`. Do not create the full child folder tree up front.

`00-control/track-context.md` records:

- parent project and path
- track purpose
- parent context files to read
- parent decisions that constrain the track
- decisions that can stay local
- decisions that must be promoted to the parent
- naming and publishing expectations

Promote decisions back to the parent when they affect product direction, target user, positioning, principles, roadmap priority, implementation requirements, launch scope, risk posture, or assumptions the parent depends on.

## Clean Handoff Mode

Use Clean Handoff Mode when you want each phase to start with fresh context, possibly on a different agent or model.

The pattern is:

`Skill/Agent 1 -> writes Markdown files and handoff -> context clears -> Skill/Agent 2 reads the handoff and minimum files -> continues`

Ask Codex:

> Use Clean Handoff Mode for this project.

Codex should then create or update `00-control/handoff.md` after each phase.

Best use cases for Clean Handoff Mode:

- `idea-o-00-import`: when the source chat or document is long.
- `idea-o-03-research`: when evidence quality matters or research is broad.
- `idea-o-07-strategy`: when target, positioning, distribution, or model choices are strategic.
- `idea-o-08-mvp`: when comparing several experiment paths.
- `idea-o-10-implementation-spec`: when implementation requirements must be clear before execution.
- `idea-o-10-execution-rules`: when AI agents need explicit boundaries before execution.
- `idea-o-11-review`: when deciding whether to continue, pivot, pause, or stop.

Less useful for Clean Handoff Mode:

- `idea-o-01-intake`: usually small enough to run inline.
- `idea-o-10-execution`: often better as quick incremental updates.
- Tiny personal projects or low-risk internal notes.

Model assignment idea:

| Skill | Suggested Model Type |
| --- | --- |
| `idea-o` | Fast general model |
| `idea-o-00-import` | Strong summarization model for long source material |
| `idea-o-01-intake` | Fast general model |
| `idea-o-02-problem` | General or stronger reasoning model |
| `idea-o-03-research` | Strong research/reasoning model |
| `idea-o-04-risks` | Strong reasoning model |
| `idea-o-05-vision` | Strong reasoning model |
| `idea-o-06-principles` | General reasoning model |
| `idea-o-07-strategy` | Strong strategy/reasoning model |
| `idea-o-08-mvp` | Strong reasoning and option-generation model |
| `idea-o-09-roadmap` | General reasoning model |
| `idea-o-10-implementation-spec` | Strong implementation planning model |
| `idea-o-10-execution-rules` | General reasoning model |
| `idea-o-10-execution` | Fast general model |
| `idea-o-11-review` | Strong reasoning model |

Use `Parallel Support` only for independent research branches, competitor scans, or option generation. One agent should integrate the results into the project files.

## Run One Phase

Ask Codex to run a specific phase, for example:

> Run the research evidence phase for this idea.

Codex should:

1. Read `00-control/current-state.md`.
2. Use the matching skill from `.agents/skills/`.
3. Create only that phase's required folder and files if they are missing.
4. Read the phase input files that exist.
5. Ask only the necessary questions.
6. Update the phase output files.
7. Log decisions and risks.
8. Apply `framework/rules/phase-quality-gates.md`.
9. Update `00-control/current-state.md`.

Codex should not mark the phase complete until required outputs are written to Markdown files or you consciously accept a logged skip with risk.

In `idea-o-03-research`, Codex should choose or ask for a research mode:

- `Founder Assumption Audit`: test what the founder currently believes.
- `End-User Questionnaire`: create interview or survey questions for target users.
- `Mixed`: use both, usually for product, service, business, and market-facing ideas.
- `Assumption-led`: choose high-risk assumptions, do decision-relevant research, log deferred research risk, and define the smallest validation step.

Every research mode must include a market scan for present solutions, substitutes, workarounds, and comparable alternatives.

When research supports a specific choice, Codex may create a research decision packet in `03-research/decision-packet.md` or a named packet. The packet should include the decision question, direct evidence, analogous evidence, counter-evidence, confidence, recommendation, and what would change the decision. Accepted recommendations must be linked from `00-control/decision-log.md`.

## Optional UX Artifacts

Create UX artifacts only when needed by the active phase. Keep them phase-local instead of creating a permanent UX track.

Optional files:

- `screen-map.md`: screens, states, entry points, exits, and unresolved screen questions.
- `copy-decisions.md`: confirmed copy, rejected copy, tone rules, and copy risks.
- `interaction-rules.md`: mode behavior, allowed actions, blocked actions, feedback, and edge cases.
- `permission-experience.md`: permission prompts, user benefit, fallback behavior, privacy concerns, and recovery paths.

When one is created, index it in `00-control/current-state.md` and log any decisions or blockers it creates.

## Skip With Risk Logging

You may skip a phase, question, or artifact. Codex must log:

- What was skipped
- Why it was skipped
- The risk created
- Who accepted the risk
- When to revisit it

Use `framework/rules/blocking-and-skipping.md` for the required format.

Skipping does not require creating the skipped phase folder. Record the risk in `00-control/current-state.md` and `00-control/open-questions.md` unless a more specific file already exists.

## Review Or Pivot

Use phase `11-review-pivot` when:

- New evidence contradicts the current direction.
- An experiment finishes.
- Progress stalls.
- Strategy, MVP, or target user needs to change.

Pivots are decisions. Record them in both `11-review/pivot-decisions.md` and `00-control/decision-log.md`.

## Publish Idea Artifacts

Use `idea-o-publish` before branching, staging, committing, pushing, or opening a PR for idea artifacts.

The publish workflow confirms:

- target idea folder
- repository root
- base branch
- branch naming convention, usually `codex/<idea-or-track-name>`
- exact files to stage
- wrong-folder prevention checks
- publish decision recorded in control files

Codex should not stage unrelated dirty worktree changes or perform git writes the user did not explicitly request.

## Repository Contents

- `framework/phases/`: phase-by-phase process guidance.
- `framework/rules/`: cross-phase rules for evidence, decisions, files, transitions, blocking, and skipping.
- `framework/index.md`: compact routing index for context-efficient navigation.
- `templates/project/`: reference file patterns for progressive creation; do not copy all files up front.
- `.agents/skills/`: Codex skills for orchestrating and running phases.
- `examples/cozyinn-demo/`: a short fictional example project.
