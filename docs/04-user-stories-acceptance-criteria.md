# Part 4 — User Stories & Acceptance Criteria

Stories are the **negotiation unit** between “what users need” and “what you will build this week.”

---

## INVEST checklist

Good stories are:

- **I**ndependent — Minimal coupling to other stories
- **N**egotiable — Details can change; outcome stays
- **V**aluable — User or business value visible
- **E**stimable — You can size S/M/L
- **S**mall — Fits one iteration
- **T**estable — Acceptance criteria exist

If not **Small**, split vertically (thin end-to-end slice) not horizontally (all backend first).

---

## Acceptance criteria formats

### Format A: Bullet checklist (fastest solo)

```markdown
- [ ] Valid email required; inline error if invalid
- [ ] Success shows "Check your inbox" without revealing if email exists
- [ ] Link expires after 24h; expired link shows renew option
```

### Format B: Gherkin (Given / When / Then)

Good for e2e tests and unambiguous behavior.

```gherkin
Scenario: Successful password reset request
  Given I am on the forgot-password page
  When I submit a registered email address
  Then I see "Check your inbox"
  And a reset email is queued within 30 seconds
```

### Format C: Examples table (rules with data)

| Input | Expected |
|-------|----------|
| qty=2, rate=10 | line total 20 |
| qty=0 | validation error |

Use for pricing, permissions, validation.

---

## Story splitting patterns

When a story feels big, split using:

| Pattern | Example |
|---------|---------|
| **Workflow steps** | Draft invoice → Send invoice → Mark paid |
| **Business rules** | Happy path vs payment declined |
| **Data variations** | Single currency → multi-currency (later) |
| **Roles** | Buyer story vs seller story |
| **Operations** | Create vs read vs update |
| **Non-functional spike** | “Spike: prove webhook idempotency” (time-boxed) |

---

## Definition of Ready (before story enters sprint)

- [ ] Linked to REQ ID(s)
- [ ] Acceptance criteria written
- [ ] Mock or API contract sketched (if UI/API)
- [ ] Dependencies identified
- [ ] Test approach noted (unit / e2e / manual)

---

## Mapping stories to requirements

Many-to-many is normal:

| Story | Requirements |
|-------|----------------|
| US-02-01 | REQ-FR-12, REQ-NFR-05 |
| US-02-02 | REQ-FR-12 |

RTM captures this (Part 7).

---

## Anti-patterns

- **Technical stories masquerading as user stories**  
  “As a developer I want Redis” → Reframe: “As a user I want cart to persist across sessions (REQ-FR-20)” with tech note in tasks.

- **Criteria that assert implementation**  
  “Uses Redux” → Instead: “State survives page refresh.”

- **Missing failure cases**  
  Always add at least one negative scenario per critical story.

---

## Estimation without fooling yourself

Use **relative points** (1, 2, 3, 5, 8) or T-shirt sizes:

- **1** — Few hours, known pattern
- **3** — Half week, some unknown
- **8** — Split; too much unknown

Track **actual vs estimate** in retro; improve decomposition, not self-blame.

Next: [Part 5 — Modules & WBS](05-modules-and-wbs.md)
