# Docs

This directory is the documentation home for `forge`.

Use it for two things:

- curated docs that should stay stable
- rough notes that are worth keeping even before they are curated

## Core Docs

- [architecture.md](architecture.md): stable project architecture overview
- [development.md](development.md): contributor operating manual for the concrete project
- [security.md](security.md): secrets, protected data, and access-boundary rules
- [references.md](references.md): curated readings that shaped `forge`

## Structured Project Docs

- [spec/README.md](spec/README.md): stable behavior and contract docs
- [designs/README.md](designs/README.md): technical design docs
- [process/README.md](process/README.md): workflow guidance and bootstrap path
- [notes/README.md](notes/README.md): append-only topical notes, discoveries,
  and operational breadcrumbs
- [../workflows/README.md](../workflows/README.md): concrete tool adapters for
  version control, tracking, and local workflow commands
- [../devhub/README.md](../devhub/README.md): lightweight internal project
  status surface

## Rule of Thumb

- use `spec/` for what should be built and why
- use `designs/` for technical choices and tradeoffs
- use `architecture.md` for the system shape as a whole
- use `development.md` for concrete contributor commands and environment rules
- use `security.md` for secrets, protected data, and access boundaries
- use `process/` for the workflow around planning, implementation, review, and commit
- use `workflows/` for tool-specific commands that implement the process
- use `devhub/` for contributor-facing status, release, benchmark, and triage surfaces
- use `notes/` when writing something quickly is better than not writing it at
  all
