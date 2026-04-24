# forge

`forge` is a repo-native operating context for software projects built by
humans and agents.

The goal is simple: after `git clone`, the repository should contain the
project's durable memory and enough operating context to make the next change
without archaeology in chat, Jira, Confluence, Google Docs, or someone's head.

It works best when a project wants:

- source-controlled specs
- source-controlled technical design docs
- explicit process around planning, implementation, review, and commit
- durable written context for humans and agents
- local-first issue and workflow state
- minimal dependence on external project-management surfaces

This is especially useful for:

- open source projects
- highly collaborative repositories
- agent-assisted development
- teams that want more spec-driven or design-driven development
- projects where behavior, decisions, and process should live in version control

That means:

- `docs/spec/` holds behavior, scope, and contract docs
- `docs/designs/` holds technical decisions and implementation plans
- `docs/process/` holds workflow guidance
- `workflows/` holds concrete tool adapters
- `devhub/` holds a lightweight project status surface when the project needs one
- top-level docs hold stable project-wide context

## Operating Biases

- Keep product intent, design history, workflow, and contributor commands in the repo.
- Prefer small executable slices over documentation theater.
- Prefer local-first, version-controlled state over external coordination systems.
- Prefer minimal dependencies and explicit operational ownership.
- Make the project understandable to a fresh human or agent from repository
  context alone.

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
