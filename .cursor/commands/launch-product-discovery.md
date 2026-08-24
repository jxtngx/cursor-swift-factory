# Launch Product Discovery (Swift factory)

Same *shape* as [cursor-fullstack-factory](https://github.com/jxtngx/cursor-fullstack-factory) and [cursor-agent-factory](https://github.com/jxtngx/cursor-agent-factory) discovery: questionnaire → technical requirements → architect → scrum.
Questions are about a **Swift app**, not a web stack or an LLM harness.

Called from `@init-app` after platform is locked. If `TRACK.md` is missing, run `@init-app` instead.

## Question sequence

### Q1 — Job

Conversational, then lock it:

- One-sentence description (what the app *does*)
- Problem statement (why a Notes clone is not enough)
- Product name

Give two examples first:

- "A field log for a hardware bench: capture measurements, photos, and part numbers offline."
- "A Watch complication plus iPhone detail for a personal interval timer."

If they describe a Watch companion while TRACK is `ios-*`, record it as a **later milestone**, not a change of TRACK.

### Q2 — Users

```
Who is the primary user?
- Individual (personal utility)
- Small team
- Customers (App Store / TestFlight)
- Mixed
```

### Q3 — Auth

```
- None
- Sign in with Apple
- Custom backend (name it)
```

### Q4 — Data

```
- On-device only (SwiftData / files)
- Sync (CloudKit / custom API)
- Read-only from a public API
```

Name entities they care about (3–7).

### Q5 — Offline

```
- Must work fully offline
- Offline cache, online source of truth
- Online-only
```

### Q6 — Monetization

```
- None
- Paid up front
- IAP / subscription (name the entitlement later)
```

### Q7 — Capabilities (platform-aware)

Ask only what the locked platform can do. Examples:

- iPhone: camera, push, background location (yes/no, must-have vs later)
- iPad: multitasking / keyboard / pointer (yes/no)
- Mac: menu bar, documents, sandbox file access
- Watch: complications, workout session, always-on

### Q8 — Non-goals

Force an out-of-scope list (at least three items).

### Q9 — Repo

- GitHub `owner/repo` for the *generated* product (may be this repo if transforming in place)
- Sprint plan filename: `<slug>-sprint.plan.md`
- Bundle ID prefix if they have one (e.g. `dev.jxtngx`) — do not invent an Apple team ID

## Write the spec

Use [technical-requirements-template.md](../templates/technical-requirements-template.md) and [platform-spec-template.md](../templates/platform-spec-template.md).

Do not implement.
Hand back to `@init-app` step 3 (review) if you were invoked from there; otherwise hand off to `@chief-architect` yourself.
