# Bootstrap Workflow

This file describes the eventual `./bootstrap` contract for a specialized
project.

The template does not provide a universal bootstrap script. Each project should
define the smallest repeatable setup path that gets a fresh human or agent to a
working local environment.

## Bootstrap Should Answer

- which runtimes and tools are required
- how dependencies are installed
- how local configuration is generated
- how secrets or tokens are requested
- which checks verify setup
- which commands are safe without internal access

## Expected Shape

```bash
./bootstrap
./<project-command> test
./<project-command> run
```

Use different commands if the project already has a standard entrypoint. Record
the real commands in `docs/development.md`.

## Agent Behavior

Agents should be able to:

- detect missing tools
- report missing credentials without printing secret values
- run the fastest setup verification
- avoid destructive environment changes unless explicitly approved

## Keep It Boring

Bootstrap should install and verify the toolchain. It should not hide complex
business logic, deploy production by default, or become a private framework.
