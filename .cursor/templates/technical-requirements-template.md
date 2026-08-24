# Technical Requirements Template (Swift factory)

Write to `.cursor/plans/project-init/[slug]-technical-requirements.plan.md`.

```markdown
---
name: [App name]
overview: [One sentence]
track: [ios-iphone | ios-ipad | ios-universal | macos | watchos]
problem_statement: [Why this app]
github_repo: [owner/repo]
bundle_id_prefix: [e.g. dev.example]
sprint_plan_file: .cursor/plans/project-init/[slug]-sprint.plan.md
todos:
  - id: spec
    content: Spec approved
    status: pending
  - id: skeleton
    content: Walking skeleton launches on locked device class
    status: pending
  - id: mvp
    content: Must-have flows + tests
    status: pending
isProject: false
---

# [App name] — Technical Requirements

## User Story

As a [user], I want [behavior] so that [benefit].

## Problem Statement

[Pain. Why a generic notes/timer/list template is not enough.]

## Platform (locked)

- **TRACK**: [ios-iphone | ios-ipad | ios-universal | macos | watchos]
- **Min OS**: [e.g. iOS 17 / macOS 14 / watchOS 10]
- **UI**: SwiftUI
- **Language**: Swift 6

See sibling `[slug]-platform.plan.md`.

## Users

- Primary: [who]
- Secondary: [who or none]

## Auth

- [none | Sign in with Apple | custom]

## Data

- Persistence: [SwiftData | GRDB | files | none]
- Sync: [none | CloudKit | custom API]
- Entities (MVP): [list]

## Offline

- [full | cache | online-only]

## Monetization

- [none | paid | IAP]

## Must-have flows (MVP)

| Flow | Device notes | Must-have |
| --- | --- | --- |
| [name] | [e.g. compact iPhone] | yes |

## Non-goals

- [ ]
- [ ]
- [ ]

## Definition of Done (MVP)

- [ ] Spec approved
- [ ] App launches on the locked device class / simulator
- [ ] Must-have flows implemented in SwiftUI
- [ ] Domain tests green without signing secrets
- [ ] Privacy usage strings listed if capabilities need them
- [ ] TRACK honored (no extra platforms)

## Next

1. @chief-architect validates
2. @swift-sme notes official APIs
3. @scrum-master writes sprint
```
