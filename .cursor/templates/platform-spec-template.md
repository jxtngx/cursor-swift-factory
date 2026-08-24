# Platform spec template

Write to `.cursor/plans/project-init/[slug]-platform.plan.md`.

```markdown
# [App name] — Platform spec

## TRACK

`[ios-iphone | ios-ipad | ios-universal | macos | watchos]`

## Device class

- iOS iPhone: compact width default; no iPad-only layout work
- iOS iPad: regular width, split view / sidebar if the spec asked
- iOS Universal: size classes; iPhone and iPad both in DoD
- macOS: WindowGroup (or DocumentGroup if documents); menu bar if specified
- watchOS: Watch app lifecycle; complications only if must-have

## Navigation

[stack | tabs | sidebar | document | watch pages]

## Capabilities (MVP vs later)

| Capability | MVP | Notes |
| --- | --- | --- |
| [camera / push / ...] | yes/no | |

## Lifecycle

SwiftUI `@main`. Note scenes, background modes, complications.

## SPM sketch

- `App` (executable / Xcode app target)
- `Domain` (pure Swift)
- `Data` (persistence)
- `Feature[Name]` as needed

## Walking skeleton

Copy guidance from `templates/[track]/` after approval. Do not copy before.

## Out of this milestone

Companion apps and extra device classes not in TRACK.
```
