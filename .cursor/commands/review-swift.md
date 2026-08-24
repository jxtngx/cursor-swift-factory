# Review Swift

PR-style review of the current ticket diff.
Critique. Do not silently rewrite the whole module.

## MUST

1. Confirm the ticket and TRACK
2. Flag: data races, force-unwrap in production paths, main-thread blocking, missing tests, UIKit-by-default, secrets
3. Check actor isolation and SPM import rules from the architecture plan
4. Accessibility on primary flows if the ticket touched UI
5. Ask engineers to fix blockers; do not expand scope

## MUST NOT

- Approve without tests the ticket required
- Soften Swift 6 concurrency
