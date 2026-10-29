# Part 6 — Prioritization

Breakdown creates options; prioritization **commits** to order.

---

## MoSCoW (MVP default)

| Label | Meaning | Rule |
|-------|---------|------|
| **Must** | MVP fails without it | ≤ 60% of effort |
| **Should** | Important, defer if slip | Next release |
| **Could** | Nice | If time |
| **Won't** | Explicit no | Write down to resist scope creep |

Every REQ and story gets one label for the current release.

---

## RICE (when comparing many ideas)

Score = (Reach × Impact × Confidence) / Effort

| Factor | Solo tip |
|--------|----------|
| Reach | Users affected per month (estimate) |
| Impact | 0.25 low → 3 massive |
| Confidence | 0.5 guess → 1.0 validated |
| Effort | Person-weeks |

Use RICE for **post-MVP** backlog ordering.

---

## Value vs risk matrix

Plot stories:

```
        High value
            │
    Quick   │   Strategic
    wins    │   bets
────────────┼────────────
    Fillers │   Time sinks
            │
        Low value
     Low effort ── High effort
```

Do **Quick wins** and **Strategic** first; kill **Time sinks** for MVP.

---

## Story slicing for delivery order

Order by:

1. **Learning** — What reduces biggest unknown? (spike first)
2. **Risk** — Legal, payments, security
3. **Revenue / core loop** — Path to “someone paid” or “someone returned”
4. **Polish** — Animations, edge cases

**Walking skeleton:** thinnest end-to-end path (login → one core action → persist data).

---

## Fixed time, variable scope

Pick release date (even arbitrary). When date is fixed, **scope flexes**:

- Must-haves ship
- Should-haves move to next milestone
- Could-haves drop

This is how solo shipping beats perfection.

---

## Saying no (template)

Add to parking lot with reason:

```markdown
- OAuth login — Won't MVP — email/password sufficient; revisit at 500 users
- Admin dashboard — Won't MVP — use SQL/scripts temporarily
```

Visible “won’t” list reduces guilt and scope creep.

Next: [Part 7 — Traceability matrix](07-traceability-matrix.md)
