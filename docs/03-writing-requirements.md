# Part 3 — Writing Requirements

Requirements are **commitments about behavior**. They use precise language and stable IDs.

---

## Requirement types

| Type | Prefix | Example |
|------|--------|---------|
| Functional (FR) | REQ-FR- | The system shall send email on successful payment |
| Non-functional (NFR) | REQ-NFR- | API p95 latency ≤ 300ms under 100 RPS |
| Constraint (CON) | REQ-CON- | Must run on PostgreSQL 15+ |
| Business rule (BR) | REQ-BR- | Refunds only within 14 days of purchase |

---

## Good requirement language

Use **shall** for mandatory, **should** for desired, **may** for optional.

| Weak | Strong |
|------|--------|
| Fast login | REQ-NFR-02: Login API p95 ≤ 500ms at 50 concurrent users |
| Secure | REQ-NFR-03: Passwords hashed with Argon2id; never logged |
| Nice onboarding | REQ-FR-05: New user completes profile in ≤ 3 form steps |

Properties of good requirements (**SMART-C**):

- **Specific** — One behavior per ID
- **Measurable** — Can test or inspect
- **Achievable** — For MVP scope
- **Relevant** — Traces to a goal
- **Time-bound** — Release or phase tag
- **Consistent** — No contradictions with other REQ IDs

---

## Requirements register structure

Maintain `docs/requirements.md` (copy [templates/requirements-register.md](../templates/requirements-register.md)):

```markdown
| ID | Type | Statement | Priority | Status | Release |
|----|------|-----------|----------|--------|---------|
| REQ-FR-01 | FR | ... | Must | Approved | MVP |
```

**Status values:** Draft → Approved → Implemented → Verified → Deprecated

Only **Approved** requirements go in MVP sprint commitments.

---

## From brainstorm to requirements

1. **Brain dump** — Unstructured list (30 min timer).
2. **Cluster** — Group by user journey (onboard → use core → account).
3. **Normalize** — Rewrite each as shall/should with ID.
4. **Dedupe** — Merge duplicates; note superseded IDs.
5. **Prioritize** — MoSCoW (Part 6).
6. **Trace** — Add RTM rows (Part 7).

---

## User journeys map to requirements

Draw a linear journey (even ASCII):

```
Land → Sign up → Onboard → Core action → Share/pay → Return
```

For each step ask:

- What must the system do? → FR
- How well must it perform? → NFR
- What must never happen? → Security / constraint

---

## Ambiguity killers

Add these fields to non-obvious requirements:

- **Source** — Who asked / which goal
- **Rationale** — Why it exists
- **Verification method** — Test, demo, inspection, analysis
- **Dependencies** — Other REQ IDs

Example:

> **REQ-FR-12:** The system shall allow password reset via email link expiring in 24 hours.  
> **Verification:** Automated e2e + manual security review.  
> **Depends on:** REQ-FR-01 (email delivery).

---

## Common mistakes

| Mistake | Fix |
|---------|-----|
| UI mockups as requirements | State behavior; link mock separately |
| “Implement React page X” | “User can view order status updated within 5s of shipment” |
| One REQ for entire module | Split by testable behaviors |
| No NFRs until production fire | Add 5 NFRs early: security, perf, backup, logging, accessibility baseline |

---

## Solo-friendly rigor level

| Phase | Requirement count (typical) |
|-------|-----------------------------|
| Weekend prototype | 5–15 FR, 3 NFR |
| MVP launch | 30–80 FR, 10–20 NFR |
| Growth | Full RTM + change control |

Start small; **IDs from day one** so you never renumber chaos.

Next: [Part 4 — User stories & acceptance criteria](04-user-stories-acceptance-criteria.md)
