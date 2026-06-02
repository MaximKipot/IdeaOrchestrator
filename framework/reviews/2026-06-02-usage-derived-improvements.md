# IDEA-O Usage-Derived Improvement Candidates

Date: 2026-06-02
Branch: `codex/idea-o-usage-patterns`
Status: Draft for user approval and refinement

## Purpose

This review looks at previous Codex sessions and durable Markdown projects where the IDEA / IDEA-O framework was used directly or indirectly. The goal is not to invent theoretical improvements. The goal is to identify changes suggested by actual usage patterns.

## Reviewed Usage Set

Method:

- Searched Codex thread summaries for `IDEA-O`, `idea-o`, `IdeaZone`, `idea-`, `00-control`, and `current-state.md`.
- Searched raw Codex JSONL sessions under `~/.codex/sessions` for IDEA-O markers, project folders, and control-file references.
- Read durable project files in:
  - `/Users/admin/Desktop/IdeaZone`
  - `/Users/admin/Desktop/CalmZone/idea`
  - `/Users/admin/Desktop/CalmZone/idea-intervention-levels`
  - `/Users/admin/Desktop/CalmZone/idea-onboarding`
  - `/Users/admin/Desktop/CalmZone-idea-calibration-contents/idea-calibration`
  - `/Users/admin/Desktop/Taflow-Timer/idea`

Direct IDEA-O sessions reviewed:

- `019e41e9`: create the original Codex-first idea framework.
- `019e63c8`: clarify Phase 10 implementation specs and agent execution rules.
- `019e5366`: import Taflow discussion material.
- `019e5533`: define Taflow problem and decisions.
- `019e561e`: research Confluence workshop planning and update Taflow risks.
- `019e53d4`: import CalmZone / CozyINN project summary.
- `019e58b9`: import and develop CalmZone intervention levels.
- `019e5e54`: research smartphone intervention rules for CalmZone.
- `019e5f3b` and `019e638d`: develop CalmZone onboarding and Usage Insights.
- `019e7c91`: develop BLE calibration as a separate idea track.

Adjacent sessions reviewed because they depended on IDEA-O artifacts or updated idea project state:

- CalmZone implementation handoff from `idea-intervention-levels` into Spec Kit.
- CalmZone debugging/review sessions around intervention behavior, BLE detection, overlay fallback, YouTube/PiP, and detection reports.
- Taflow strategy and technical feasibility updates after research.
- Branch/publish requests for whole idea folders.

## High-Level Pattern

The framework is useful because it keeps project memory in files. The strongest benefit showed up when decisions were later needed for implementation, debugging, or review.

The main strain is that real usage does not stay inside a clean phase sequence. Work repeatedly moved between idea development, research, UX copy, implementation contracts, Spec Kit, code debugging, branch publishing, and review. The framework should keep the sequential model, but add clearer "escape hatches" for these real transitions.

## Recommended First Improvements

These are the highest leverage changes to approve first.

| Priority | Improvement | Usage Pattern | Candidate Change |
|---|---|---|---|
| P0 | Make framework rules resolvable from installed skills, not only project folders. | External projects recorded notes like `framework/rules/phase-quality-gates.md was not present in this workspace`. | Skills should resolve rules relative to the skill/framework installation, then optionally copy or link a short rule reference into the project. |
| P0 | Add an official implementation handoff path. | CalmZone needed `10-implementation-spec/ai-implementation-contract.md`, a Spec Kit prompt, and explicit "do not mix planning systems" instructions. | Add `idea-o-10-implementation-spec` and `idea-o-10-execution-rules` as first-class handoff steps with consistent file naming, Spec Kit prompt output, and "ask at forks" behavior. |
| P0 | Add current-state compaction rules. | `current-state.md` became a long encyclopedia in `idea-intervention-levels`. It is useful, but hard to scan. | Split into a short dashboard plus linked detail files. Require `current-state.md` to show only current phase, last update, active decisions, blockers, and next action. |
| P1 | Add decision lifecycle support. | Decision logs accumulated many superseded rows, especially typed-intention and Protect friction decisions. | Add `active`, `superseded`, `rejected`, `deferred`, and `revisit trigger` fields. Add a "current active decisions" summary so agents do not accidentally revive old decisions. |
| P1 | Add open-question triage. | Open-question files grew into long mixed backlogs across product, technical, UX, and validation questions. | Require a "Blocking next action" section, "Answer soon" section, and "Parking lot" section. Each question gets owner, phase, and revisit trigger. |

## Candidate Improvements

### 1. Skill-relative rule lookup

Observed evidence:

- CalmZone import/current-state files explicitly noted that `framework/rules/phase-quality-gates.md` was not present in that workspace.
- IDEA-O projects live inside product repos such as `CalmZone` and `Taflow-Timer`, not always inside `IdeaZone`.

Improvement:

- Every skill should know how to find framework rules from the installed skill directory or the framework repo.
- If rules are missing in the project workspace, the agent should not treat that as a failure. It should use the installed rule source and optionally write a short note.

Why it matters:

- Quality gates and context-efficiency rules are core behavior. They should not depend on the user copying the framework folder into every idea project.

### 2. Official implementation handoff

Observed evidence:

- The user asked whether the flow should ask for implementation specs and execution rules.
- CalmZone intervention work created `10-implementation-spec/ai-implementation-contract.md`.
- A later implementation prompt explicitly told Codex: use Spec Kit only, do not mix Superpowers planning, treat the implementation contract as authoritative.

Improvement:

- Add an official handoff artifact that can generate:
  - implementation contract
  - agent execution rules
  - Spec Kit compatible prompt
  - verification expectations
  - non-goals and forbidden assumptions

Why it matters:

- IDEA-O is strong at product memory, but real use immediately needs implementation transfer. The handoff should be repeatable instead of reconstructed manually.

### 3. Current-state dashboard format

Observed evidence:

- `idea-intervention-levels/00-control/current-state.md` captured a lot of useful context, but grew very long.
- Agents need fast orientation, not a full project narrative every time.

Improvement:

- Change `current-state.md` to a compact dashboard:
  - project
  - current phase
  - last update
  - current focus
  - active decisions
  - blocking questions
  - files changed last
  - next recommended action
- Move long historical summaries into phase files or `00-control/project-history.md`.

Why it matters:

- The framework's source-of-truth rule only works if the source of truth stays quickly readable.

### 4. Decision lifecycle and supersession rules

Observed evidence:

- CalmZone intervention decisions evolved several times: typed intention was confirmed, later removed; Protect emergency friction changed; Check-in behavior changed.
- The decision log preserved history, but agents must distinguish active decisions from superseded decisions.

Improvement:

- Add a structured decision lifecycle:
  - `Active`
  - `Superseded`
  - `Rejected`
  - `Deferred`
  - `Archived`
- Require superseded decisions to link to the replacing decision.
- Add an "Active decisions only" table near the top.

Why it matters:

- Preserving rejected or superseded choices is good. Accidentally implementing them later is bad.

### 5. Open-question triage

Observed evidence:

- Taflow and CalmZone open-question files became broad mixed lists.
- Some questions blocked the next decision; others were background risks.

Improvement:

- Add question sections:
  - `Blocking Next Action`
  - `Decision Needed Soon`
  - `Research Later`
  - `Parking Lot`
  - `Resolved`
- Each question should include owner, phase, status, and revisit trigger.

Why it matters:

- The user should not have to parse 30 questions to know what to answer next.

### 6. Sub-idea track support

Observed evidence:

- CalmZone split into several idea tracks: base idea, intervention levels, onboarding, calibration.
- Calibration was explicitly started as a separate track instead of mixing into the parent idea folder.

Improvement:

- Add a lightweight "sub-idea track" rule:
  - parent project
  - track purpose
  - parent context files to read
  - what decisions can be local
  - what decisions must be promoted to parent
  - how to name and publish the folder

Why it matters:

- Real product work branches into focused idea tracks. The framework should support that without losing the parent product memory.

### 7. Branch and publish safety for idea folders

Observed evidence:

- The user asked to create a separate branch and commit an entire idea folder using Spec Kit naming.
- This is a recurring need when idea artifacts are ready to preserve or hand off.

Improvement:

- Add an `idea-o-publish` or publishing checklist:
  - confirm target folder
  - confirm branch naming convention
  - confirm base branch
  - list files to stage
  - prevent wrong-folder commits
  - record publish decision in the control files

Why it matters:

- IDEA-O artifacts are deliverables. Publishing them should be safe and explicit.

### 8. Research-to-decision packets

Observed evidence:

- User asked: "what is the evidence to make this decision?"
- User asked onboarding work not to rely only on the current app, but also on intervention-levels research.
- Taflow research changed product direction by showing comparable agenda timer products existed.

Improvement:

- Add a small decision packet format:
  - decision question
  - evidence directly supporting it
  - analogous evidence
  - counter-evidence
  - confidence
  - recommendation
  - what would change the decision

Why it matters:

- Research is most valuable when it changes a decision, narrows a risk, or prevents a weak assumption from becoming a plan.

### 9. Experience design lane without a rigid new track

Observed evidence:

- CalmZone onboarding work became screen-by-screen product design.
- Intervention-level work needed copy options, future ideas, behavioral distinctions, and UX warnings.
- These files did not fit perfectly into existing phase names.

Improvement:

- Add optional phase-local UX artifacts:
  - `screen-map.md`
  - `copy-decisions.md`
  - `interaction-rules.md`
  - `permission-experience.md`
- Keep them just-in-time, not mandatory.

Why it matters:

- Product ideas often become UX flows before they become specs. The framework should make that durable without forcing a full design system.

### 10. "Modes must feel different" challenge

Observed evidence:

- The user challenged Check-in, Pause, and Protect because they felt too similar.
- The later refinement made the levels psychologically distinct: awareness, regulation, boundary.

Improvement:

- In MVP/UX phases, add a mode-differentiation check:
  - What job does each mode do?
  - What does the user feel in each mode?
  - What action is uniquely allowed or blocked?
  - What would make two modes collapse into one?

Why it matters:

- Many product ideas create tiers or modes. The framework should force a practical distinction test before implementation.

### 11. Execution evidence capture

Observed evidence:

- Debugging sessions produced important product/technical decisions:
  - media-safe silent transitions
  - RSSI freshness fallback
  - overlay versus Activity fallback behavior
  - YouTube/PiP overlay edge cases
- Some of these were later reflected in idea files; others depended on implementation specs and code review threads.

Improvement:

- Add a small Phase 10 capture routine:
  - new evidence from build/test/debug
  - decision changed?
  - assumption invalidated?
  - user-visible behavior changed?
  - update current state and decision log

Why it matters:

- Implementation teaches the idea. The framework should capture that feedback loop without forcing the user back through earlier phases.

### 12. Import fidelity choice

Observed evidence:

- CalmZone import noted that a faithful structured summary was preserved, but not the full verbatim transcript.
- The file logged skip risk: exact phrasing might be lost.

Improvement:

- At import, choose one of:
  - `Verbatim Preservation`
  - `Structured Faithful Summary`
  - `Decision-Focused Summary`
- Log why, what was omitted, and what risk remains.

Why it matters:

- Users often start from large chats. The framework should be explicit about whether exact wording is preserved.

### 13. Assumption-led fast mode

Observed evidence:

- Taflow explicitly chose assumption-led development to move fast.
- Research remained mandatory, but broad research was narrowed by risk.

Improvement:

- Add a documented `Assumption-led` depth mode:
  - choose high-risk assumptions
  - do only decision-relevant research
  - log deferred research risk
  - define the smallest validation step

Why it matters:

- "Research is mandatory" should not mean "research everything before moving." Real use prefers momentum with explicit risk.

### 14. Custom artifact indexing

Observed evidence:

- Useful custom files appeared:
  - `copy-options.md`
  - `future-ideas.md`
  - `technical-feasibility.md`
  - `platform-compliance-reality-check.md`
  - `calibration-flow-concept.md`
  - `existing-usage-access-integration.md`
- Current-state sometimes listed these, but this was not a formal rule.

Improvement:

- Allow custom phase-local artifacts, but require `current-state.md` to index each custom file with:
  - purpose
  - status
  - owner
  - next use

Why it matters:

- The framework should stay flexible without making important custom files invisible.

### 15. Direct-answer plus persistence rule

Observed evidence:

- Many sessions were not clean phase starts. The user asked direct questions inside idea folders, such as whether Miro should be first or whether Check-in differed enough from Pause and Protect.
- The best outcomes answered directly and then updated files when the conclusion changed the project.

Improvement:

- Add a rule:
  - answer the direct question first when the user asks for reasoning
  - update project files only if a decision, risk, evidence, or next action changes
  - do not force every direct question into a phase ceremony

Why it matters:

- IDEA-O should support natural thinking conversations while still preserving durable outcomes.

## Candidate Non-Goals

Do not turn IDEA-O into a heavy project management system.

Do not create every optional artifact up front.

Do not split the universal sequence into many rigid tracks.

Do not make research deeper by default. Make it more decision-relevant.

Do not replace Spec Kit or implementation planning tools. Make IDEA-O handoff into them cleaner.

## Suggested Approval Order

1. Approve rule lookup and current-state compaction first.
2. Approve implementation handoff and execution evidence capture second.
3. Approve decision lifecycle and open-question triage third.
4. Approve sub-idea track and publish workflow fourth.
5. Approve optional UX artifacts, research packets, and assumption-led mode fifth.

## Open Questions For Approval

1. Should these improvements be implemented as framework rule changes first, or as skill changes first?
2. Should `10-implementation-spec` remain a separate folder, or should implementation prep live under `10-execution/`?
3. Should there be a dedicated `idea-o-publish` skill, or only a publishing rule used by `idea-o`?
4. Should sub-idea tracks have a required parent pointer file?
5. Should the next implementation pass update existing example projects, or only templates and skills?
