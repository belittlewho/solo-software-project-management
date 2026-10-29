# Part 17 — Testing, Quality & Verification

Requirements are worthless without **verification method**. This part closes the gap between RTM and actual QA.

---

## V&V quick distinction

| Verification | Validation |
|--------------|------------|
| Built right (spec) | Built right thing (user need) |
| Tests vs REQ | Interviews, beta feedback |
| You do both solo | Discovery + RTM Verified |

---

## Test pyramid (solo realistic)

```
        /  E2E  \        few — critical journeys
       / integration \   some — API + DB
      /    unit      \   many — rules, math, auth
```

| Layer | Proves | ID prefix |
|-------|--------|-----------|
| Unit | Business rules, pure logic | TEST-UNIT- |
| Integration | Modules + DB + external mocks | TEST-INT- |
| E2E | User journeys vs AC | TEST-E2E- |
| Manual | Exploratory, UX, visual | TEST-MAN- |

Every **Must** REQ needs ≥1 of: automated test ID or **signed manual checklist** in RTM.

Template: [templates/test-plan-lite.md](../templates/test-plan-lite.md)

---

## Mapping AC → tests

| Acceptance criterion | Test |
|----------------------|------|
| Given invalid email, show error | TEST-UNIT-02, TEST-E2E-01 |
| Payment fails → cart preserved | TEST-E2E-04 |

Duplicate AC text in test description for searchability.

---

## Test case format

| Field | Value |
|-------|--------|
| ID | TEST-E2E-03 |
| REQ | REQ-FR-12 |
| Story | US-01-03 |
| Steps | 1. … 2. … |
| Expected | … |
| Automatable | yes/no |

---

## Regression strategy

- **Smoke suite** — 5–15 min, runs every PR  
- **Full regression** — before release tag  
- **Visual** — optional screenshot diff for UI-heavy  

Tag flaky tests; fix or quarantine — flaky E2E erodes trust in RTM.

---

## Quality attributes (link to NFR)

| Attribute | Example REQ | Test approach |
|-----------|-------------|---------------|
| Performance | REQ-NFR-01 p95 | k6 / Lighthouse |
| Security | REQ-NFR-10 auth | OWASP checklist, dependency scan |
| Accessibility | REQ-NFR-11 WCAG 2.1 AA | axe, manual keyboard |
| Reliability | REQ-NFR-05 uptime | monitoring SLO |

See [Part 21 — NFR catalog](21-security-privacy-compliance-nfr-catalog.md).

---

## Bug vs story vs REQ

| Item | When |
|------|------|
| Bug | Behavior violated **approved** REQ or AC |
| Story | New behavior |
| REQ change | Spec wrong — update register + RTM first |

Bug ticket: `REQ-FR-05 regression`, link commit that broke trace.

---

## Definition of Verified (REQ status)

REQ moves to **Verified** when:

- [ ] Linked tests pass in CI **or** manual evidence filed (`docs/test-evidence/v1/`)  
- [ ] RTM row complete  
- [ ] No open P0 against that REQ  

Next: [Part 18 — Architecture traceability](18-architecture-design-traceability.md)
