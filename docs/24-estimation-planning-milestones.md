# Part 24 — Estimation, Planning & Milestones

Breakdown without time reality checks leads to endless MVP. Estimation is **risk management**, not prophecy.

---

## What to estimate

| Object | Method |
|--------|--------|
| Epic | T-shirt or range (S/M/L) |
| Story | Points 1–8 |
| Task | Hours (≤ 8) |
| Milestone | Calendar date with buffer |

Never estimate entire project in hours on day 1 — estimate **next sprint** and **next milestone**.

---

## Story points (Fibonacci)

| Points | Meaning |
|--------|---------|
| 1 | Trivial, done before |
| 2 | Straightforward |
| 3 | Normal |
| 5 | Unknowns |
| 8 | Split required |
| 13 | Epic in disguise |

Points reflect **effort + uncertainty**, not hours alone.

---

## Three-point estimate (tasks)

Optimistic (O), Most likely (M), Pessimistic (P):

**Expected = (O + 4M + P) / 6**

Use for milestones with external dependencies (app review, legal).

---

## Buffer rules

- MVP milestone: add **25–40%** buffer solo (illness, unknowns)  
- Single-threaded: critical path = sum of Must stories on longest dependency chain  

---

## Milestone planning

```markdown
## M1 — Private beta (target: 2026-12-01)
Exit criteria:
- REQ-FR-01..15 Verified
- 5 users completed core journey
Dependencies:
- D-01 payment sandbox approved
Buffer: 1 week
```

Work backward from exit criteria → required stories → order by dependency.

---

## Cone of uncertainty

Early estimates are wrong — that is expected. Re-estimate every sprint using **actual** velocity.

---

## Fixed scope vs fixed date

| Fixed date | Fixed scope |
|------------|-------------|
| Cut Should/Could | Move date |
| Must-only for launch | Add resources (hard solo) |

Default solo: **fixed date for learning milestones**, flex scope.

Next: [Part 25 — Roadmaps & OKRs](25-roadmaps-okrs-themes.md)
