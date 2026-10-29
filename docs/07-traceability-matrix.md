# Part 7 — Traceability Matrix (RTM)

A **Requirements Traceability Matrix (RTM)** answers: *If this requirement changes, what breaks? If this test fails, what requirement is unmet?*

---

## Why solo engineers need an RTM

Without traceability:

- You forget why code exists
- Refactors delete critical behavior silently
- “Done” means different things each week

With a lightweight RTM:

- Every REQ links to ≥ 1 story and ≥ 1 verification
- Releases become checklists, not hope

---

## Minimum RTM columns

| Req ID | Requirement summary | Story IDs | Design / ADR | Code location | Test IDs | Release | Status |

**Code location:** file path, module, or PR link — not line numbers (they drift).

**Test IDs:** `TEST-UNIT-12`, `TEST-E2E-03`, or pytest node id.

---

## Forward vs backward traceability

| Direction | Question |
|-----------|----------|
| **Forward** | REQ-FR-01 → which stories, code, tests? |
| **Backward** | TEST-E2E-03 → which REQ does it prove? |

Both must hold for **Verified** status on a requirement.

---

## Building RTM incrementally (do not big-bang)

1. **Day 1:** REQ IDs + empty RTM table in repo
2. **Each story:** Add row when story is created
3. **Each PR:** Update Code + Test columns
4. **Each release:** Mark Verified or gap list

Gap list example: “REQ-FR-08 — no automated test — manual checklist only.”

---

## Example row

| Req ID | Summary | Stories | Design | Code | Tests | Release | Status |
|--------|---------|---------|--------|------|-------|---------|--------|
| REQ-FR-12 | Password reset email 24h expiry | US-01-03 | ADR-002 auth | `packages/auth/reset.ts` | TEST-E2E-05 | MVP | Verified |

---

## Coverage metrics (simple)

- **Req coverage** = reqs with ≥1 test / total approved reqs
- **Test orphan rate** = tests with no REQ / total tests

Target for MVP launch: **≥ 90% Must reqs verified**, zero orphan Must tests.

---

## Tools

| Tool | RTM approach |
|------|----------------|
| Markdown in repo | Copy [templates/traceability-matrix.md](../templates/traceability-matrix.md) |
| GitHub Issues | Label `req:FR-12`; link in body |
| Notion / Sheets | Same columns; link to repo |
| Jira / Linear | Custom field “Requirement ID” |

**Single source of truth:** pick one; mirror IDs everywhere else.

---

## RTM + Git workflow

PR template snippet:

```markdown
## Traceability
- REQ: REQ-FR-__
- Tests: TEST-__
- RTM updated: yes/no
```

Commit message optional tag: `[REQ-FR-12]`.

---

## When RTM feels heavy

Use **RTM-Lite** for prototypes:

| Req | Story | Test |
|-----|-------|------|

Three columns only. Expand when you onboard users or handle money.

Next: [Part 8 — Backlog & Definition of Done](08-backlog-and-dod.md)
