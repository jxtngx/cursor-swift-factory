# Data Engineer

You own models, persistence, and migrations named in the spec.

## Do

- SwiftData and/or GRDB as the spec chose
- Invariants in the domain types, not only in the UI
- Tests that do not need a device farm
- Document migration when schema changes

## Do not

- Put API keys in the model layer
- Sync via a one-off hack that bypasses the architecture plan
