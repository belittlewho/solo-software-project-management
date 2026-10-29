# Part 22 — Stakeholders & Communication

Solo does not mean no stakeholders — **future you**, users, co-founders, clients, and platform vendors all count.

---

## Stakeholder map

| Stakeholder | Interest | Influence | Communication |
|-------------|----------|-----------|---------------|
| Primary user | Usable product | High | Interviews, beta |
| You (future maintainer) | Clean RTM | High | ADRs, docs |
| Payment provider | Compliance | Medium | Their docs + REQ |
| Host (Vercel/AWS) | Uptime | Medium | Status page |

Update when adding B2B customers (buyer vs user personas).

---

## RACI lite (solo)

| Activity | R | A | C | I |
|----------|---|---|---|---|
| REQ approval | You | You | User advisor | — |
| Release | You | You | — | Users (notes) |

When a collaborator joins, split **R** and **A** explicitly.

---

## Status update template (async)

Weekly for clients or accountability partner:

```markdown
## Week of DATE
**Goal:** G-1 progress
**Shipped:** US-… (link PR)
**Verified REQs:** REQ-FR-…
**Next:** …
**Risks:** R-…
**Decisions needed:** …
```

Ties code to REQ IDs — professional and traceable.

---

## Scope change conversation

When someone asks for a feature:

1. Capture in Inbox  
2. Classify MoSCoW for **current** milestone  
3. If Must-add: what Must-remove or date slip?  
4. Update charter non-goals or REQ register with version  
5. Never “sure” without RTM impact note  

---

## Conflict between requirements

| Situation | Resolution |
|-----------|------------|
| REQ A contradicts REQ B | Deprecate one; ADR or charter call |
| User A vs User B | Primary persona wins MVP |
| Speed vs security | NFR minimum bar non-negotiable; scope feature |

Document resolution in change log.

Next: [Part 23 — Tooling](23-tooling-github-linear-notion.md)
