# Part 21 — Security, Privacy & NFR Catalog

Engineers forget NFRs because they are **not features**. Use this catalog when writing MVP — tick applicable rows into your register.

---

## Security (baseline)

| ID suggestion | Statement (adapt) |
|---------------|-------------------|
| REQ-NFR-SEC-01 | All traffic TLS 1.2+ in production |
| REQ-NFR-SEC-02 | Secrets only in env / secret manager |
| REQ-NFR-SEC-03 | Passwords hashed (Argon2/bcrypt); never logged |
| REQ-NFR-SEC-04 | Session invalidation on logout |
| REQ-NFR-SEC-05 | RBAC: users access only own resources |
| REQ-NFR-SEC-06 | Dependency vulnerability scan in CI |
| REQ-NFR-SEC-07 | Rate limit auth endpoints |
| REQ-NFR-SEC-08 | CSRF protection on cookie auth |
| REQ-NFR-SEC-09 | Input validation server-side |

Verification: OWASP ASVS level 1 checklist, pen test for money/health.

---

## Privacy (if you store PII)

| ID | Statement |
|----|-----------|
| REQ-NFR-PRI-01 | Privacy policy published |
| REQ-NFR-PRI-02 | Collect minimum PII |
| REQ-NFR-PRI-03 | User can export data |
| REQ-NFR-PRI-04 | User can delete account + data |
| REQ-NFR-PRI-05 | Retention period defined |

Map to GDPR/CCPA if EU/CA users — legal review beyond this guide.

---

## Performance

| ID | Statement pattern |
|----|-------------------|
| REQ-NFR-PERF-01 | Core page LCP ≤ 2.5s on 4G |
| REQ-NFR-PERF-02 | API p95 ≤ 300ms at N RPS |
| REQ-NFR-PERF-03 | Background job completes within X min |

Define **N** for your expected load; revise after beta metrics.

---

## Reliability & availability

| ID | Statement |
|----|-----------|
| REQ-NFR-REL-01 | Target uptime 99.5% (solo reasonable) |
| REQ-NFR-REL-02 | RPO ≤ 24h, RTO ≤ 4h (adjust) |
| REQ-NFR-REL-03 | Idempotent webhooks |

---

## Accessibility

| ID | Statement |
|----|-----------|
| REQ-NFR-A11Y-01 | WCAG 2.1 AA for core flows |
| REQ-NFR-A11Y-02 | Keyboard navigable checkout/auth |

---

## Maintainability

| ID | Statement |
|----|-----------|
| REQ-NFR-MAIN-01 | Lint + typecheck in CI |
| REQ-NFR-MAIN-02 | Critical modules have unit tests |
| REQ-NFR-MAIN-03 | ADR for architectural forks |

---

## Compliance hooks (when applicable)

| Domain | Extra artifacts |
|--------|-----------------|
| Payments | PCI scope minimization, no PAN storage |
| Health | HIPAA — expert required |
| SOC2 | Extended RTM + evidence folders |

Part 12 covers audit-style RTM.

---

## NFR → RTM

NFRs often span many stories. RTM: one NFR row → **multiple** TEST-* or **audit checklist** file.

Next: [Part 22 — Stakeholders](22-stakeholders-communication.md)
