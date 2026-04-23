# Agentic Development Process

This directory documents the operating process for `forge`.

## Overview

The default workflow is:

```
understand -> plan/design -> approve -> implement -> review -> commit
```

Read only the document needed for the task in front of you.

## Golden Path

If the repo is still a generic template, start with
[bootstrap.md](bootstrap.md).

If the repo is already specialized or the task is ordinary project work:

| Task | Document |
|------|----------|
| Plan or design the work | [planning.md](planning.md) |
| Implement approved work | [implementation.md](implementation.md) |
| Review a change | [code-review.md](code-review.md) |
| Prepare a commit | [committing.md](committing.md) |
| Use or replace default local tracking | [issue-tracking.md](issue-tracking.md) |

## Work Types

### Small Work

- 1-3 files or one bounded change
- one focused session
- no ADR needed

Workflow:

```
understand -> plan -> approve -> bd issue -> implement -> review -> commit
```

### Large Work

- broad technical change
- multiple phases or sessions
- meaningful design tradeoffs

Workflow:

```
understand -> plan/design -> approve -> spec and/or ADR + bd epic/subtasks -> implement -> review -> commit
```

## Principles

- approval before formal tracking
- `docs/spec/` is for stable behavior and contracts
- `docs/designs/` is for technical decisions and phases
- ADRs for large technical work only
- `jj` and `bd` are defaults, not universal requirements
- spec updates when behavior, scope, or product intent needs a stable written contract
- main should stay releasable
- CI should be thin and build-system-first
- delivery rules should stay explicit and low-noise enough to trust
