# Decision Log Rules

Decisions are durable project memory. If it matters later, write it down.

## Required Format

Use this format in `00-control/decision-log.md`:

```markdown
# Decision Log

## Active Decisions Summary

| ID | Decision | Phase | Date | Revisit Trigger |
| --- | --- | --- | --- | --- |

## YYYY-MM-DD - Short Decision Name

- Classification: Decision
- Status: Active | Superseded | Rejected | Deferred | Archived
- Decision:
- Context:
- Options Considered:
- Evidence Used:
- Tradeoffs:
- Consequences:
- Supersedes:
- Superseded By:
- Revisit Trigger:
```

## What Counts As A Decision

- Target user selection
- Problem framing
- Research depth
- Positioning
- MVP or experiment choice
- Constraints
- Strategy
- Roadmap priority
- Research recommendation accepted from a decision packet
- Execution evidence changing behavior, scope, assumptions, or implementation direction
- Publishing or branch-scope decision for idea artifacts
- Pivot, pause, or stop choice

## Rules

- Preserve rejected options.
- Do not rewrite history. Add dated updates instead.
- If a decision changes, add a new decision entry, mark the old one `Superseded`, and link the old and replacement entries both ways.
- Link research decision packets and execution evidence captures in `Evidence Used` when they support the decision.
- Keep the top active-decision summary current. It should include only decisions whose status is `Active`.
- Use `Deferred` for choices intentionally postponed, `Rejected` for considered choices not selected, and `Archived` for decisions no longer relevant to the live project.
