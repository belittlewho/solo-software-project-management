# Part 9 — Risks, Assumptions & Dependencies

Breakdown is incomplete without **what could be wrong**.

---

## RAID log (solo scale)

| Type | ID | Description | Impact | Likelihood | Mitigation | Owner |
|------|-----|-------------|--------|------------|------------|-------|
| Risk | R-01 | Payment provider delays approval | High | Med | Start Stripe test mode week 1 | You |
| Assumption | A-01 | Users have email | Med | High | Validate in interviews | You |
| Issue | I-01 | (active problems) | | | | |
| Dependency | D-01 | Domain DNS for prod | Med | Low | Buy domain early | You |

Review in weekly planning (Part 10).

---

## Assumption → requirement

If assumption fails, product fails. Promote critical assumptions to **spikes** or **REQ**:

> Assumption: “Sellers will upload CSV.”  
> Spike: 3 seller interviews + prototype upload → pass/fail before EP-03.

---

## Technical spikes

**Spike story format:**

- Time-box: 4–8 hours max
- Output: decision doc (ADR) or throwaway code
- Not “done” until recommendation written

Link spike to REQ or epic blocked.

---

## ADR (Architecture Decision Record)

One page per big decision:

```markdown
# ADR-003: Use Medusa for commerce backend

## Status
Accepted

## Context
…

## Decision
…

## Consequences
…

## Requirements affected
REQ-FR-01, REQ-CON-02
```

ADRs appear in RTM **Design** column.

---

## External dependencies

Track:

- API keys / approvals
- Third-party SLAs
- Legal (terms, privacy)
- App store review timelines

Add **buffer** to milestone dates for externals you do not control.

Next: [Part 10 — Solo execution rhythm](10-solo-execution-rhythm.md)
