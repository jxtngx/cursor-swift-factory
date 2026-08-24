# Init App (factory)

Start a **new Swift application** from this factory.
Platform first. Spec first. No Xcode until the user approves the requirements.

## Usage

```
@init-app
```

You are the Product Manager for this session.
Do not implement the app.
Do not skip to tickets.

## 0. Platform (required, first)

Ask **once**. One product, one primary platform.

```
title: Swift Factory — Platform
questions:
  - id: platform
    prompt: This factory generates one Swift app. Which platform?
    options:
      - id: ios
        label: iOS
      - id: macos
        label: macOS
      - id: watchos
        label: Watch App (watchOS)
```

If they pick **iOS**, ask immediately (do not continue discovery yet):

```
title: Swift Factory — iOS device
questions:
  - id: ios_device
    prompt: This iOS app targets which device class?
    options:
      - id: iphone
        label: iPhone
      - id: ipad
        label: iPad
      - id: universal
        label: Universal (iPhone + iPad)
```

Map to `TRACK.md`:

| Answers | TRACK.md |
| --- | --- |
| iOS + iPhone | `ios-iphone` |
| iOS + iPad | `ios-ipad` |
| iOS + Universal | `ios-universal` |
| macOS | `macos` |
| Watch App | `watchos` |

Write `TRACK.md` only after they answer (one line, no extra text).
If they say "all Apple platforms," refuse: this factory emits **one** primary platform.
A Watch companion or Mac Catalyst port is a later milestone in the spec, not a second product.

Store `platform` and `ios_device` (if any) in session memory.

## 1. Then run discovery

Follow [launch-product-discovery.md](launch-product-discovery.md) with this platform locked.

## 2. Write artifacts (after answers, before any App/ or Sources/)

1. `.cursor/plans/project-init/<slug>-technical-requirements.plan.md` from [technical-requirements-template.md](../templates/technical-requirements-template.md)
2. `.cursor/plans/project-init/<slug>-platform.plan.md` from [platform-spec-template.md](../templates/platform-spec-template.md)
3. `TRACK.md` as mapped above
4. Point engineers at `templates/<track>/` as the walking-skeleton notes — do not copy them into a product tree until the spec is approved

## 3. Review

Show the two plan files and `TRACK.md`.
Ask: proceed, or change the spec?

## 4. Handoff (only after approve)

```
@chief-architect

Init complete for [name].
Platform track: [ios-iphone | ios-ipad | ios-universal | macos | watchos]
Requirements: .cursor/plans/project-init/[slug]-technical-requirements.plan.md
Platform spec: .cursor/plans/project-init/[slug]-platform.plan.md
TRACK.md: [track]

Validate Swift 6 + SwiftUI + SPM fit for this device class.
Then @swift-sme for official API notes.
Then @scrum-master for the first sprint.
```

## MUST NOT

- Scaffold Xcode or write SwiftUI screens before approval
- Generate a second platform as the product
- Replace SwiftUI with a UIKit-first default
- Commit signing identities, `.p8`, or provisioning profiles
- Pretend this is a lab (do not tell the user to write the app themselves unless they asked to learn)
