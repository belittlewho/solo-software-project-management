# Part 1 — Foundations

## What you are learning

Two different skills get mixed up:

| Skill | Question it answers |
|--------|---------------------|
| **Software engineering** | How do I implement this correctly? |
| **Project / requirements engineering** | What exactly should exist, for whom, and how do we know it is done? |

You can be strong at the first and weak at the second. That is normal. Implementation rewards **depth**; breakdown rewards **breadth and clarity**.

---

## Why solo engineers fail at breakdown

Common patterns:

1. **Solution-first thinking** — You picture React components or database tables before naming the user outcome. The brain skips “what problem” and jumps to “how I’d build it.”
2. **No stable IDs** — Requirements live in your head or chat logs. Nothing links “login” to “test AUTH-12” to “PR #44.”
3. **Infinite granularity** — Either everything is one giant “build the app” task, or you explode into 200 micro-tasks with no hierarchy.
4. **Perfection as scope** — “Real” products need auth, admin, analytics, mobile, i18n… before anyone uses v0.
5. **No definition of done** — Work never ends because “done” was never written.

Breakdown is a **writing and naming** discipline, not IQ.

---

## Core artifacts (you will use all of these)

```
Vision / Problem statement
        ↓
Goals & success metrics
        ↓
Scope (MVP vs later) + Non-goals
        ↓
Requirements (numbered: REQ-xxx)
        ↓
Features / Epics (grouped capabilities)
        ↓
User stories + Acceptance criteria
        ↓
Tasks (implementation units)
        ↓
Traceability matrix (links reqs ↔ stories ↔ tests ↔ releases)
```

You do not need enterprise tools. Markdown files in your repo are enough.

---

## The “OUTCOME → OUTPUT → ACTIVITY” filter

When you write a backlog item, label it:

- **Outcome** — User or business result (“Customer receives order confirmation email within 60s”).
- **Output** — Deliverable artifact (“Email template + send on `order.placed`”).
- **Activity** — Work step (“Research Resend API”).

**Backlog items for shipping should be Outcomes or Outputs**, not vague Activities.

Bad: “Work on checkout.”  
Better: “Buyer can pay with Mobile Money and see receipt (REQ-CHK-03).”

---

## Vertical slices vs horizontal layers

| Horizontal (layer) | Vertical (slice) |
|--------------------|------------------|
| “Build all API endpoints” | “User can reset password end-to-end” |
| “Set up database schema” | “Guest can complete one purchase” |
| “Design system components” | “Seller can list one product with photo” |

Prefer **vertical slices** for MVP. Layers still exist inside each slice, but planning in layers delays feedback.

---

## Minimum vocabulary

- **Requirement** — A statement of need (shall/should/must). Has an ID.
- **Feature** — A coherent capability users recognize (“Password reset”).
- **User story** — Short narrative: role, need, reason. Has acceptance criteria.
- **Epic** — Large feature container (multiple stories).
- **Task** — Concrete work unit, usually ≤ 1 day.
- **RTM (Requirements Traceability Matrix)** — Table linking requirements to design, code, and tests.
- **NFR** — Non-functional requirement (performance, security, availability).
- **MVP** — Minimum set that validates the core hypothesis.

---

## Exercise (15 minutes)

Pick any side project. Write only these four lines:

1. **User:** …
2. **Problem:** …
3. **Success in 30 days:** …
4. **Explicitly not building yet:** …

Stop. Do not open your IDE. If you cannot fill line 4, you will scope-creep — that is valuable data.

Next: [Part 2 — The decomposition ladder](02-decomposition-ladder.md)
