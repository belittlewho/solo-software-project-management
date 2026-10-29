# Part 20 — Release, DevOps & Operations

Shipping is a **requirement**. Operability NFRs belong in the register from day one.

---

## Environments

| Env | Purpose | Data |
|-----|---------|------|
| Local | Dev | Seed / fake |
| Staging | Pre-prod verification | Anonymized copy or synthetic |
| Production | Users | Real |

REQ-CON: “No production secrets in repo.” REQ-NFR: staging mirrors prod topology.

---

## Release checklist (solo)

- [ ] All Must REQs **Verified** or **waived** (written in RTM)  
- [ ] Migrations tested rollback  
- [ ] Feature flags for risky EP-* (optional)  
- [ ] Release notes (user-facing)  
- [ ] Tag git `v1.0.0` + RTM snapshot `docs/releases/v1.0.0-rtm.md`  
- [ ] Smoke test on prod  
- [ ] Monitoring alerts configured  

---

## Deployment strategies (know the names)

| Strategy | Solo use |
|----------|----------|
| Big bang | Small MVP ok |
| Rolling | Default many PaaS |
| Blue/green | Zero-downtime when you have traffic |
| Canary | % rollout when risk high |

Link deployment REQ-NFR to runbook steps.

---

## Runbook (minimum)

`docs/runbook.md`:

- How to deploy  
- How to rollback (exact commands)  
- Where logs/metrics live  
- On-call: you — escalation contacts  
- Known failure modes  

---

## Observability NFRs

| REQ type | Example |
|----------|---------|
| Logging | Structured JSON; request ID |
| Metrics | Error rate, latency p95 |
| Alerting | Page on 5xx spike |
| Backup | DB daily; restore tested quarterly |

Add to register before launch, not after outage.

---

## CI/CD traceability

- CI runs TEST-* linked to changed modules  
- Failed main blocks release  
- PR template: REQ IDs  

---

## Post-release

- Monitor 24–48 h  
- Capture bugs as REQ regressions  
- Retro: what broke traceability?  

Next: [Part 21 — NFR catalog](21-security-privacy-compliance-nfr-catalog.md)
