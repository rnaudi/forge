# forge

`forge` is a documentation-first bootstrap for collaborative software projects.

It works best when a project wants:

- source-controlled specs
- source-controlled technical design records
- explicit process around planning, implementation, review, and commit
- durable written context for humans and agents
- less reliance on tribal memory and ephemeral chat context

This is especially useful for:

- open source projects
- highly collaborative repositories
- agent-assisted development
- teams that want more spec-driven or design-driven development
- projects where behavior, decisions, and process should live in version control

The goal is simple: make the repository itself the shared operating context.

That means:

- `docs/spec/` holds behavior, scope, and contract docs
- `docs/designs/` holds technical decisions and phased implementation records
- `docs/process/` holds workflow guidance
- `workflows/` holds concrete tool adapters
- top-level docs hold stable project-wide context

## Agent Entry Point

Start at `AGENTS.md`.

If the repo is still generic, the next document is:

- `docs/process/bootstrap.md`

Otherwise continue with:

1. `docs/README.md`
2. `docs/process/README.md`
3. `workflows/README.md` if the task needs concrete tool commands
4. the single task-specific process doc you need

The repo aims to be neutral across agent interfaces. Tool defaults live in
`workflows/` so projects can replace them without rewriting the process docs.
