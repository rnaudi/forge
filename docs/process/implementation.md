# Implementing Work

This document describes how to implement approved work.

## Prerequisites

Before implementing:

1. a plan exists
2. large work has the required spec and/or ADR artifacts
3. the work is small enough for one session, or has been split

## Step 1: Load Context

1. Get the issue details:

```bash
bd show <bd-id> --json
```

2. For large work, read the relevant spec in `docs/spec/` and the ADR in
   `docs/designs/` when present.

3. Mark the issue as in progress:

```bash
bd update <bd-id> --status in_progress --json
```

## Step 2: Scope Check

Proceed when the work is:

- clear
- bounded
- one logical unit

Split it when:

- the change spans too many files
- unrelated concerns are mixed together
- too much discovery is still needed

If needed, create subtasks:

```bash
bd create "Subtask: <description>" --parent <bd-id> -t task --json
```

## Step 3: Recommended Order

1. Update specs if this changes stable behavior, contracts, or product-facing
   scope.
2. Update architecture or development docs if the project-wide shape or
   contributor workflow changed.
3. Add or update tests first when practical.
4. Make code changes.
5. Run the fastest relevant verification.
6. For large work, update the ADR phase checklist.

## Step 4: Verify

Run the project-appropriate checks. Prefer the smallest command that gives real
confidence first, then broader checks before commit.

Examples:

- unit tests
- integration tests
- lint
- typecheck
- build

## Step 5: Update Progress

For large work, update the ADR checklist:

```markdown
## Implementation Phases

- [x] **Phase 1: Name** - bd-42
- [ ] **Phase 2: Name** - bd-43
```

## Step 6: Review and Commit

Before committing:

1. follow `code-review.md`
2. fix blocking issues
3. follow `committing.md`

## Important

- each commit should leave the repo in a coherent state
- split oversized work instead of forcing it through one session
- stable behavior changes should usually have spec documentation
- major technical direction changes should usually have ADR documentation
