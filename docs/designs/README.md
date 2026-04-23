# Technical Design Docs and ADRs

This directory contains numbered technical design records for large changes.

These documents are ADR-like: they capture technical decisions after the
problem and product intent are clear enough to choose an implementation
direction.

## What an ADR Captures

- context
- the decision
- goals and non-goals
- alternatives considered
- implementation phases
- consequences and tradeoffs

## When to Write One

Write an ADR for work that:

- spans multiple sessions
- has meaningful design choices
- needs phased delivery
- benefits from a durable historical record

Do not write an ADR for small, obvious changes.

## Lifecycle

```
proposal -> accepted -> implemented -> superseded
```

## Creating an ADR

1. Copy the template:

```bash
cp docs/designs/0000-template.md docs/designs/NNNN-<title>.md
```

2. Use the next available 4-digit number.

3. Fill in:

- Summary
- Context
- Goals / Non-goals
- Decision
- Alternatives Considered
- Implementation Phases
- Consequences

4. After approval, create `bd` tracking and add issue IDs to the ADR.

## Relationship to Specs

Use ADRs for technical design decisions. Use `docs/spec/` for functional-spec /
RFD-style behavior and scope documents that should outlive the implementation
details.
