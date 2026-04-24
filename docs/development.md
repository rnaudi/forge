# Development Guide

This document is for concrete project commands and environment rules once the
stack is known.

## Purpose

Update this document when the user specifies:

- programming language
- framework
- build system
- test commands
- local run commands
- formatting and linting tools
- deployment or environment conventions

If the repo is still generic, follow `docs/process/bootstrap.md` first.

Keep this file short and concrete. If a section is not true for the project,
replace or delete it.

## Fill These Sections with Real Commands

### Build

```bash
# TBD until the project chooses a build system.
```

### Test

```bash
# TBD until the project chooses a test command.
```

### Fast Feedback Loop

```bash
# TBD until the project identifies the smallest useful local check.
```

### Run Locally

```bash
# TBD until the project has a local run command.
```

### Tidy

```bash
# TBD until the project chooses formatting, linting, or tidy commands.
```

The implementation of `tidy` depends on the stack.

## Testing Strategy

Default philosophy:

- tests should buy confidence in behavior, not decorate coverage numbers
- prefer integration tests around meaningful behavior when practical
- use unit tests for tricky logic, edge cases, and fast feedback
- avoid testing implementation details that should be free to change
- keep one fast verification path for everyday work

Fill in:

- unit test conventions
- integration test conventions
- end-to-end test conventions
- fixture or test data rules
- what every change must verify before commit
- fast vs slow test split

## Dependencies

Fill in:

- dependency manager and lockfile policy
- single source of truth for versions
- rules for adding a dependency
- rules for updating dependencies
- vulnerability scanning or audit commands
- how transitive dependencies are reviewed
- project-specific verification required before upgrades ship

## Coding Conventions

Fill in:

- formatting tools
- linting tools
- naming conventions
- package or module conventions
- error handling conventions
- searchability and naming rules that matter for this project

## Environment

Document:

- required runtimes and versions
- local services
- secrets handling for development
- database or queue setup

## Bootstrap

Document:

- setup command
- required tools
- generated local files
- required credentials and where to request them
- verification command after bootstrap

## Troubleshooting

Capture recurring setup or workflow issues here once they are known.
