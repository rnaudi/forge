# AGENTS.md

This repository is a bootstrap for agentic software projects.

Treat it as a template, not as an already-specialized project.

Do not invent stack details until the user provides concrete constraints such
as:

- language and framework
- build system
- test strategy
- deployment environment
- architectural constraints
- product or feature scope

## Purpose

This repo exists to hold:

- a start-of-session contract for agents
- reusable process docs
- project document templates
- spec and ADR templates

It should stay generic until the user asks to specialize it.

## Entry Point

Start here at the beginning of every new session.

Use this decision rule:

- if the repo is still generic, read `docs/process/bootstrap.md` next
- otherwise, read `docs/README.md`, then `docs/process/README.md`, then the
  single task-specific process doc you need

Task-specific docs:

- planning or design work: `docs/process/planning.md`
- implementation work: `docs/process/implementation.md`
- review work: `docs/process/code-review.md`
- commit work: `docs/process/committing.md`

Do not read the whole repo by default.

## Working Rules

1. Prefer updating templates over adding project-specific assumptions.
2. Keep process docs in `docs/process/`.
3. Keep large design records in `docs/designs/`.
4. Keep stable behavioral documentation in `docs/spec/`.
5. Put high-level project operating context in `docs/development.md`.
6. Put system shape in `docs/architecture.md`.

## Document Taxonomy

- `docs/spec/` is for stable behavior, scope, and external contracts
- `docs/designs/` is for technical decisions, tradeoffs, and implementation phases
- `docs/architecture.md` is the project-wide structural overview
- `docs/development.md` is the concrete project's build, test, run, and environment guide
- `docs/process/` is for workflow rules used while shaping and changing the project
- `docs/notes/` is for low-friction notes that are not yet curated docs

## Canonical Lifecycle

Use this lifecycle everywhere in the repo:

```text
understand -> plan/design -> approve -> implement -> review -> commit
```

Definitions:

- `understand`: gather enough context to avoid blind work
- `plan/design`: decide whether the work needs a brief plan, a spec, an ADR, or both
- `approve`: get approval before formal tracking and implementation
- `implement`: execute one coherent bounded slice
- `review`: check correctness, risk, and drift from the approved artifacts
- `commit`: create a clean commit and update tracking

Do not skip straight to implementation when the problem or scope is still
unclear.

## Default Tooling

Default workflow assumptions in this template:

- version control: `jj`
- work tracking: `bd`

These are defaults, not universal requirements.

## Portability

This repo is intended to be agent-interface neutral: Codex, Claude, OpenCode,
or another agent should be able to follow the same documentation structure.

It is not tooling-neutral by default. Until specialized, it carries explicit
workflow opinions such as `jj`, `bd`, approval-before-tracking, and
documentation-first planning.
