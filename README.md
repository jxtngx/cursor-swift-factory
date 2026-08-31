# Cursor Swift Factory

A **factory**, not a lab.

This repo is boilerplate for a new Swift application.
Cursor's team implements from a spec you write in the first session.

> **Lab** = student writes the code. Mentors quiz and review.
> **Factory** = you define requirements. Chief Architect, SME, Scrum, and engineers ship tickets.

Sister factories: [cursor-langchain-factory](https://github.com/jxtngx/cursor-langchain-factory) · [cursor-fullstack-factory](https://github.com/jxtngx/cursor-fullstack-factory) · [cursor-deep-learning-factory](https://github.com/jxtngx/cursor-deep-learning-factory).

This factory is tightly coupled to **Swift 6**, **SwiftUI**, and **Swift Package Manager**.
One generated product, one primary platform.

If you wanted to *learn* Swift by typing every type yourself, that would be a lab. This is not that.

---

## First command

Open this repo in Cursor and run:

```
@init-app
```

That command:

1. Asks **iOS, macOS, or Watch App** (one generated product, one primary platform)
2. If **iOS**, asks **iPhone, iPad, or Universal**
3. Walks the same style of **requirements interview** as [cursor-fullstack-factory](https://github.com/jxtngx/cursor-fullstack-factory) / [cursor-langchain-factory](https://github.com/jxtngx/cursor-langchain-factory)
4. Writes `.cursor/plans/project-init/<name>-technical-requirements.plan.md`
5. Writes `TRACK.md` (`ios-iphone` | `ios-ipad` | `ios-universal` | `macos` | `watchos`)
6. Hands off to `@chief-architect` → `@swift-sme` → `@scrum-master` → tickets

Do not ask an engineer to "just scaffold Xcode" before the spec exists.
That is the whole point of spec-driven init.

---

## Opinionated stack (not optional)

| Layer | Choice |
| --- | --- |
| Language | Swift 6, strict concurrency |
| UI | SwiftUI |
| Modules | Swift Package Manager feature packages |
| Concurrency | `async`/`await`, actors — not GCD-first |
| Persistence | SwiftData and/or GRDB / SQLite as justified in the spec |
| Networking | URLSession + typed clients; OpenAPI-generated when a schema exists |
| Tests | XCTest + Swift Testing |
| Secrets | xcconfig / env. Never in git |

You may add packages the spec names.
You may not replace SwiftUI with UIKit-first as the default without an ADR and Product Owner approval.

---

## Team

| Agent | Job |
| --- | --- |
| Product Manager | `@init-app` / `@launch-product-discovery` — spec only |
| Chief Architect | Feasibility, SPM module map, platform target, concurrency ownership |
| Swift SME | Official Swift / Apple APIs, SwiftUI lifecycle, privacy manifests |
| Scrum Master | Sprint + tickets from the spec |
| Feature Engineer | SwiftUI flows + domain logic |
| Platform Engineer | Xcode / SPM / CI / SwiftFormat / SwiftLint |
| Data Engineer | Models, persistence, migrations |
| Test Engineer | XCTest / Swift Testing, accessibility on primary flows |
| Reviewer | Correctness, actor isolation, API design, test gaps |

Engineers **do** implement here. That is the factory contract.
They implement *the spec*, not a surprise architecture.

---

## After init (typical)

```
@init-app
  → approve technical requirements
@chief-architect
@swift-sme
@scrum-master
@run-ticket-plan
@review-swift
```

---

## Repo layout (this boilerplate)

```
.cursor/
  commands/     init-app, launch-product-discovery, run-ticket-plan, review-swift
  agents/       factory team
  templates/    technical-requirements, platform spec, sprint guide
  plans/project-init/   generated specs land here
templates/
  ios-iphone/   walking-skeleton notes (used after spec)
  ios-ipad/
  ios-universal/
  macos/
  watchos/
TRACK.md        written at init (platform lock)
```

The platforms you did **not** pick stay in `templates/` as reference and are not the product.

---

## Related repos

| Repo | Kind |
| --- | --- |
| [cursor-langchain-factory](https://github.com/jxtngx/cursor-langchain-factory) | Factory — LangChain agents |
| [cursor-fullstack-factory](https://github.com/jxtngx/cursor-fullstack-factory) | Factory — fullstack product |
| [cursor-deep-learning-factory](https://github.com/jxtngx/cursor-deep-learning-factory) | Factory — PyTorch / HF |
| [cursor-rust-lab](https://github.com/jxtngx/cursor-rust-lab) | Lab — you write the code |
| [cursor-cuda-lab](https://github.com/jxtngx/cursor-cuda-lab) | Lab |
| [cursor-langchain-lab](https://github.com/jxtngx/cursor-langchain-lab) | Lab |
| [cursor-robotics-lab](https://github.com/jxtngx/cursor-robotics-lab) | Lab |

---

## License

Apache-2.0. See [LICENSE](LICENSE).
Not affiliated with Apple.
