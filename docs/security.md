# Security and Protected Data

This document describes how the concrete project handles secrets, protected
data, and access boundaries.

Keep this file practical. Do not invent controls before the project has chosen
real infrastructure, data classes, or deployment environments.

## Defaults

- Do not commit secrets, tokens, credentials, or private keys.
- Do not commit production data unless the project has an explicit protected
  data workflow.
- Prefer generated local configuration over checked-in secrets.
- Keep access requirements discoverable from the repo, even when the actual
  secret values live elsewhere.

## Bootstrap Requirements

When the project needs credentials or internal access, document:

- which credentials are required
- where a human obtains access
- how local configuration is generated
- how agents should detect missing access
- which commands are safe to run without secrets

## Protected Data

If specs, fixtures, recordings, or datasets contain sensitive information,
document:

- data classification
- storage location
- access rules
- redaction or anonymization process
- retention and deletion expectations
- whether agents may read, transform, or generate the data

## Open Questions

This template does not yet define a Git-native protected-data layer. Until a
project chooses one, keep protected data out of the repo and link to the
approved storage and access process.
