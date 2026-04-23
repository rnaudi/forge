# Planning Work

This document describes how to plan and design new work.

The key document split is:

- `docs/spec/` for stable behavior, scope, and contracts
- `docs/designs/` for technical decisions, tradeoffs, and phased implementation

## When to Plan

Plan before implementing when:

- adding new features
- making significant architectural or workflow changes
- requirements or scope are still fuzzy
- the work could span multiple sessions

Skip formal planning for:

- trivial fixes with obvious solutions
- typo-only documentation changes
- mechanical edits with no design choice

## Step 1: Understand the Work

Before planning, make sure you understand:

1. What problem is being solved?
2. What outcome is desired?
3. What already exists in the repo or docs?
4. Is there related ready work in `bd`?
5. Is this primarily a product/behavior question, a technical implementation
   question, or both?

Ask clarifying questions if the scope is ambiguous.

## Step 2: Assess Size

### Small Work

Characteristics:

- touches a small number of files
- one concept or bounded change
- can fit in one focused session
- no ADR required

Output:

- short implementation plan
- one `bd` issue after approval

### Large Work

Characteristics:

- multiple files or systems
- multiple implementation phases
- meaningful design tradeoffs
- likely to span sessions

Output:

- spec in `docs/spec/` when product behavior, scope, or user
  impact must be made explicit
- ADR in `docs/designs/NNNN-<title>.md` when technical approach or
  implementation tradeoffs must be chosen
- `bd` epic plus subtasks after approval

## Step 3: Create the Plan

### For Small Work

Create a brief plan that states:

- what will change
- likely files or areas affected
- tests or validation needed
- risks or unknowns

After approval:

```bash
bd create "<title>" -t feature -p 2 --json
```

### For Large Work

1. Decide which artifacts are required:

- **Spec only** when the core problem is product behavior, user-facing flow,
  workflow definition, or contract definition
- **ADR only** when the problem is mainly technical and the product behavior is
  already clear
- **Spec + ADR** when product intent and technical approach both need explicit
  treatment

2. If a spec is needed, start from the templates in `docs/spec/`.

The spec should cover:

- problem and scope
- goals and non-goals
- user or operator impact
- constraints
- open questions
- acceptance criteria or stable behavioral expectations

3. If an ADR is needed, copy the ADR template:

```bash
cp docs/designs/0000-template.md docs/designs/NNNN-<title>.md
```

4. Fill in the key ADR sections:

- Summary
- Context
- Goals / Non-goals
- Decision
- Alternatives Considered
- Implementation Phases
- Consequences

5. Present the draft and wait for approval.

6. After approval, create tracking:

```bash
bd create "<title>" -t epic -p 2 --json
bd create "Phase 1: <desc>" -t task --parent <epic-id> --json
bd create "Phase 2: <desc>" -t task --parent <epic-id> --json
```

7. Update the ADR with issue IDs.

## Step 4: Get Approval

Do not create `bd` tracking until the user approves the plan, spec, or ADR.

That keeps exploration cheap and avoids cluttering the tracker with abandoned
ideas.

## Output Summary

| Work Size | Artifacts |
|-----------|-----------|
| Small | brief plan + one `bd` issue |
| Large | spec and/or ADR + `bd` epic + subtasks |

## Next Step

Once approved:

- small work: implement the single approved issue
- large work: implement the first approved phase or subtask
