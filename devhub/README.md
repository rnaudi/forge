# DevHub

DevHub is the project's lightweight internal surface.

Use it when the project needs a repo-native place to expose status that
contributors and agents should see quickly, such as:

- release rotation or release status
- benchmark, fuzzing, or quality signals
- triage queues
- known broken checks
- links to active specs, design docs, and work items

Keep DevHub generated or maintained from repository state where practical.
Avoid turning it into a second documentation hierarchy.

## Suggested Starting Point

For a newly specialized project, start with one page that answers:

- what is currently releasable
- what is blocked
- what needs triage
- which checks matter before commit
- which docs define the current product and design direction
