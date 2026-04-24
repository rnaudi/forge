# CI Workflow

This workflow records the project's mechanical checks once a concrete stack is
known.

Keep CI thin, build-system-first, and low-noise.

## Green Main

The preferred invariant is:

```text
main only advances to commits whose required checks are known to pass
```

Use a merge queue, protected branch, or project-specific equivalent when the
team needs one. Do not make humans repeatedly reconcile stale CI by hand.

## Required Checks

Document the smallest set of checks that protects main:

- build
- fastest meaningful test suite
- formatting or tidy checks
- lint or static analysis when it catches real defects
- generated-code or docs consistency checks when applicable

## Tidy Checks

Use a `tidy` command or equivalent for project-specific mechanical rules that
are easier to automate than remember.

Good tidy checks are boring and high-signal:

- no generated drift
- no forbidden large files
- no stale placeholders
- no broken links in curated docs
- no unsupported dependency versions

## Dependency Automation

Avoid alert and PR noise.

Prefer targeted checks that identify real risk:

- vulnerability checks filtered to reachable or relevant dependencies when the
  ecosystem supports it
- scheduled latest-dependency test runs
- explicit review before dependency upgrades are committed
- project-specific validation before production rollout
