# Run Ticket Plan

Implement the **next** ticket from the current sprint plan.
Factory engineers write code. They implement the spec, not a new architecture.

## Usage

```
@run-ticket-plan
```

## MUST

1. Read `TRACK.md`
2. Read `.cursor/plans/project-init/*-technical-requirements.plan.md`, `*-platform.plan.md`, and the sprint plan
3. Pick the first open ticket
4. Implement **only** that ticket for the locked platform
5. Tests must run without Apple Developer secrets
6. Swift 6 / SwiftUI / SPM as specified
7. Stop and summarize the diff

## MUST NOT

- Skip the spec
- Add a second platform target "while we are here"
- Replace SwiftUI as the default UI
- Commit `.p8`, profiles, or `.env`
- Tell the user to write the feature themselves (this is a factory)
