# Project Architecture

This document describes the stable system shape of the project once the stack
and boundaries are known.

This document is a stable project overview, not a replacement for:

- `docs/spec/` behavior and contract docs
- `docs/designs/` design docs for specific technical decisions

## Overview

Provide a short description of the system:

- what it does
- who or what uses it
- the main technical shape

Example:

> This project is a backend service built with `<framework>` that exposes
> `<interfaces>` and coordinates `<main responsibilities>`.

## System Context

Describe the system at the highest useful level:

- clients or users
- external systems
- upstream dependencies
- downstream dependencies

## High-Level Architecture

Describe the main parts of the system and how they interact.

Example areas:

- API layer
- application/service layer
- domain logic
- persistence layer
- background jobs
- integration adapters

## Request / Data Flow

Walk through one representative end-to-end flow.

Suggested structure:

1. input enters the system
2. validation / parsing happens
3. domain logic runs
4. persistence or external calls happen
5. output is returned or published

## Major Components

For each major component, capture:

- purpose
- responsibilities
- key interfaces
- important constraints

## Data Model

Document the main data shapes and ownership boundaries:

- primary entities
- ownership boundaries
- persistence model if relevant

## Operational Concerns

Document constraints such as:

- latency or throughput goals
- reliability requirements
- scaling model
- security constraints
- observability expectations

## Build and Runtime Boundaries

Describe:

- main modules or packages
- deployable units
- internal libraries
- generated code or assets if relevant

## References

- related specs in `docs/spec/`
- related design docs in `docs/designs/`
