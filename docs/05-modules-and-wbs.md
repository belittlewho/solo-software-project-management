# Part 5 — Modules, Bounded Contexts & WBS

**Features** are what users see. **Modules** are how you organize code and team boundaries. For solo work, modules prevent spaghetti.

---

## Feature breakdown vs technical breakdown

| Feature breakdown (what) | Technical breakdown (how) |
|--------------------------|-----------------------------|
| User can checkout | `payments`, `orders`, `catalog` modules |
| Password reset | `auth`, `notifications` |

Do **feature breakdown first**, then assign modules in a second pass.

---

## Module identification (solo heuristic)

List **nouns** in your domain (Invoice, Client, Payment, Shipment). Each noun is a candidate **module** or **bounded context**.

Ask per noun:

1. Who creates / reads / updates it?
2. What invariants must always hold? (e.g. “paid total = sum(line items)”)
3. What events does it emit? (`InvoiceSent`, `PaymentCaptured`)

If two nouns share many invariants and lifecycle, they may be one module. If teams (future you vs future contractor) would argue ownership, split.

---

## Suggested repo layout (example)

```
apps/
  web/                 # UI
packages/
  domain-invoices/     # entities, use cases
  domain-payments/
  infra-email/         # adapters
  shared-kernel/       # IDs, money type, errors
```

Map modules to epics loosely — not 1:1 required.

---

## Work Breakdown Structure (WBS)

WBS is a **tree of deliverables**, not a task list of activities.

```
1.0 MVP Release
  1.1 Authentication
    1.1.1 Password reset feature
      1.1.1.1 US-01-03 stories...
  1.2 Checkout
    1.2.1 ...
```

**WBS rules:**

- Each node is a **noun** (deliverable), not “coding”
- Child nodes are **100% of parent scope** (MECE: mutually exclusive, collectively exhaustive)
- Number nodes for traceability (`1.2.1` ↔ documentation)

For software, WBS leaves often **are** user stories or feature folders.

---

## Dependency mapping

Create `docs/dependencies.md`:

| From | To | Type | Notes |
|------|-----|------|-------|
| US-03-02 Checkout | US-02-01 Catalog browse | Finish-to-start | Need product ID |
| EP-02 Payments | Spike SPIKE-01 | Start-to-start | Provider selection |

**Types:** FS (finish→start), SS, FF — use FS for 90% of cases.

Critical path = longest chain of FS dependencies → drives your milestone date.

---

## Interface contracts between modules

When you split modules, write **thin contracts**:

- API route + OpenAPI snippet
- Event schema (JSON)
- Shared types package

Requirement: **REQ-CON-04:** Cross-module calls go through published APIs in `packages/*/api`; no deep imports across domains.

---

## When to merge modules

Merge if:

- Circular dependencies appear
- You always change A and B together
- Module has < 3 stories and no clear boundary

Split if:

- File > ~500 lines and mixed reasons to change
- Tests require booting half the app

Next: [Part 6 — Prioritization](06-prioritization.md)
