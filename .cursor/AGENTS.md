# AGENTS.md — Cursor Swift Factory

This repository is a **factory**, not a lab.

Canonical contract: [cursor-langchain-factory](https://github.com/jxtngx/cursor-langchain-factory).

> **Lab** = the human writes the code. Mentors quiz and review.
> **Factory** = the human defines requirements. Chief Architect, SME, Scrum Master, and engineers **ship tickets**.

## Before the spec

Only `@init-app` / `@launch-product-discovery`.
No Xcode project, no SwiftUI screens, no Package.swift product code.

## After the spec is approved

Engineers implement the ticket.
Do not send the Product Owner to type the app themselves.
If they wanted that, they would open a lab.

## Platform lock

`TRACK.md` is the source of truth after init:

- `ios-iphone`
- `ios-ipad`
- `ios-universal`
- `macos`
- `watchos`

One product, one primary platform. Do not scaffold the other templates as the app.

## Stack

Swift 6, SwiftUI, SPM, strict concurrency.
Cite Apple / Swift.org over blogs.
No secrets in git.

## Markdown

No emojis. Semantic line breaks (one sentence per line).
