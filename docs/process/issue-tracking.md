# Issue Tracking with bd

This workflow uses [bd (beads)](https://github.com/steveyegge/beads) for local,
version-controlled issue tracking.

## Why bd

- local-first
- dependency-aware
- works well with agents
- JSON output is scriptable

## Quick Reference

```bash
bd ready --json
bd create "Title" -t feature -p 2 --json
bd create "Subtask" --parent <epic-id> --json
bd update <id> --status in_progress --json
bd close <id> --reason "Completed" --json
bd show <id> --json
```

## Lifecycle

```
open -> in_progress -> closed
```

## Workflow Rules

1. Do not create issues before approval.
2. Small work gets one issue.
3. Large work gets one epic plus subtasks.
4. Close issues before the commit that completes them when practical.

## Epics and Subtasks

For large work:

```bash
bd create "Large change" -t epic -p 2 --json
bd create "Phase 1: <desc>" -t task --parent <epic-id> --json
bd create "Phase 2: <desc>" -t task --parent <epic-id> --json
```

## Best Practices

- use `--json` for automation
- keep titles short and clear
- put deep reasoning in ADRs, not issue text
- commit `.beads/issues.jsonl` with related code or docs changes
