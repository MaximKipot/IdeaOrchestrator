# Clean Handoff Rules

Clean Handoff Mode starts each phase from files instead of chat context.

## Modes

| Mode | Use When | Behavior |
| --- | --- | --- |
| `Inline` | Small or fast-moving work | Same agent continues; still updates files. |
| `Clean Handoff` | Research, strategy, MVP, pivot, or long discussions | Current skill writes a handoff; next agent/model reads only required files. |
| `Parallel Support` | Independent research branches or option generation | Separate agents explore bounded subtasks; one agent integrates results. |

Default to `Inline` for small projects. Use `Clean Handoff` when clarity matters more than speed.

## Required Handoff Block

When Clean Handoff Mode is active, update `00-control/handoff.md`:

```markdown
# Handoff

- Completed Phase:
- Files Updated:
- Confirmed Decisions:
- Key Facts:
- Key Assumptions:
- Open Questions:
- Skipped Items / Risks:
- Recommended Next Skill:
- Minimum Files Next Skill Must Read:
```

## Next Agent Read Order

The next agent/model reads:

1. `00-control/current-state.md`
2. `00-control/handoff.md`
3. Minimum files listed in the handoff
4. `00-control/open-questions.md` only if blocked or unclear

Do not read the previous chat transcript unless the handoff says it is required.

## Quality Rules

- Decisions must be confirmed in `00-control/decision-log.md`, not only in handoff.
- Open questions must be in `00-control/open-questions.md`, not only in handoff.
- Skips and risks must be logged before handoff.
- Handoff should be short enough to read in one pass.

