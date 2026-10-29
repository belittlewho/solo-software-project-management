# Part 8 — Backlog, Milestones & Definition of Done

---

## Backlog structure

```
Inbox (unsorted ideas)
  ↓ refine weekly
Product backlog (prioritized, REQ-linked)
  ↓ pull into
Sprint / iteration backlog (committed)
  ↓
Done
```

**Inbox rule:** Anything new goes to Inbox first — not straight to “building.”

---

## Milestones (solo)

Name milestones by **outcome**, not date alone:

| Milestone | Exit criteria |
|-----------|---------------|
| M0 — Walking skeleton | One user completes core loop in staging |
| M1 — Private beta | 5 real users, feedback doc |
| M2 — Public MVP | Must reqs verified; monitoring on |

Each milestone = subset of REQ IDs marked for that release in RTM.

---

## Definition of Done (DoD) — story level

Default checklist (adapt per project):

- [ ] Acceptance criteria met
- [ ] Unit tests for business logic added/updated
- [ ] e2e or manual test noted in RTM
- [ ] No known P0 bugs
- [ ] Docs / README updated if behavior user-visible
- [ ] REQ status → Implemented (Verified after test pass)

---

## Definition of Done — release level

- [ ] All **Must** REQs Verified or waived with written reason
- [ ] RTM reviewed; gaps documented
- [ ] Migrations / rollback plan
- [ ] Secrets not in repo; env documented
- [ ] Smoke test on production-like env

---

## WIP limits

Max **2 stories In Progress**. Third story waits until one finishes.

Why: solo context-switching mimics multitasking teams — WIP limits force finish.

---

## Backlog refinement (30 min / week)

1. Pull top 10 from Inbox → rewrite as stories or discard
2. Ensure REQ IDs on Must items
3. Re-MoSCoW if deadline moved
4. Split any story > 5 points

---

## Issue / ticket template

```markdown
**Type:** story | bug | spike | chore
**REQ:** REQ-FR-__
**Epic:** EP-__

### User story
As a … I want … so that …

### Acceptance criteria
- …

### Notes / design
…

### Tasks
- [ ] …
```

Next: [Part 9 — Risks, assumptions, dependencies](09-risks-assumptions-dependencies.md)
