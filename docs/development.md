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

## Replace These Sections with Real Commands

### Build

```bash
# Example placeholders. Replace with the actual build command.
./gradlew build
# or
npm run build
# or
cargo build
```

### Test

```bash
# Replace with the default verification command.
./gradlew test
# or
npm test
# or
cargo test
```

### Fast Feedback Loop

```bash
# Replace with the smallest useful local check.
./gradlew test --tests "com.example.FastTestSuite"
# or
npm run test:unit
# or
cargo test -p crate_name
```

### Run Locally

```bash
# Replace with the local run command.
./gradlew bootRun
# or
npm run dev
# or
cargo run
```

### Tidy

```bash
# Replace with project-specific mechanical checks.
make tidy
# or
./gradlew tidy
# or
deno task tidy
```

The implementation of `tidy` depends on the stack.

## Testing Strategy

Fill in:

- unit test conventions
- integration test conventions
- end-to-end test conventions
- fixture or test data rules
- what every change must verify before commit

- fast vs slow test split
- what every change must verify before commit

## Coding Conventions

Fill in:

- formatting tools
- linting tools
- naming conventions
- package or module conventions
- error handling conventions

## Environment

Document:

- required runtimes and versions
- local services
- secrets handling for development
- database or queue setup

## Troubleshooting

Capture recurring setup or workflow issues here once they are known.
