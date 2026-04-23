# Committing Changes

This document describes how to create commits in this workflow.

## Prerequisites

Before committing:

1. relevant verification passed
2. review is complete
3. no blocking issues remain

## Version Control

This template defaults to **Jujutsu (`jj`)**.

Key differences from git:

- the working copy is always a commit
- there is no staging area
- use `jj` commands to inspect and finalize work

## Commit Message Guidelines

Format:

```text
<summary line>

<optional body>
```

Summary line:

- imperative mood
- concise
- no period at the end

Body:

- explain what and why
- avoid file lists
- avoid restating the diff

Footer:

- reference `bd` issues when useful

Examples:

```text
Add design template for large changes
```

```text
Refine implementation workflow

Clarify how approved plans become bd issues and how large work
updates ADR phase checklists.

Related to bd-42
```

## Workflow

### 1. Close Related Issues

If the project uses `bd` and the commit completes an issue:

```bash
bd close <bd-id> --reason "Completed"
```

### 2. Create the Commit

```bash
jj commit -m "<message>"
```

### 3. Verify

```bash
jj log -r @-
jj status
```

## Commit Quality

Each commit should be:

- complete
- focused
- reviewable

Do not commit:

- debug leftovers
- partial work without an intentional reason
- unrelated edits bundled together
