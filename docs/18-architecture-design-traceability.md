# Part 18 — Architecture & Design Traceability

Code structure should **trace back** to requirements, not float separately from the RTM.

---

## Layers of design (solo)

| Level | Artifact | Traces to |
|-------|----------|-----------|
| Context | Context diagram | Stakeholders, externals |
| Containers | Web, API, DB | Epics / NFR scale |
| Components | Modules in repo | Features, WBS |
| Code | Files, packages | Stories, tasks |

Use C4 mentally; draw only when communication or complexity demands.

---

## ADR workflow

1. Trigger: decision costly to reverse (DB, auth, monolith vs split)  
2. Write [ADR template in Part 9](09-risks-assumptions-dependencies.md)  
3. List **requirements affected**  
4. Link ADR in RTM **Design** column  
5. Supersede with ADR-00X if reversed — never delete old ADR  

---

## API contract as requirement

API endpoints are **outputs**, not replacements for REQs.

Pattern:

- REQ-FR-20: User shall retrieve order status by ID  
- Design: `GET /orders/{id}` OpenAPI spec  
- RTM: `openapi/orders.yaml`, `TEST-INT-07`  

OpenAPI changes require REQ or version bump note.

---

## Data model traceability

Entity checklist per table/collection:

| Entity | REQ IDs | Invariants (BR) | Owner module |
|--------|---------|-----------------|--------------|
| Order | REQ-FR-08… | total ≥ 0 | orders |

Migrations reference REQ when adding fields for compliance.

---

## UI design traceability

- Figma frame ID in story  
- AC reference **behavior**, not pixel-perfect unless REQ says so  
- REQ-NFR for accessibility applies to all screens  

---

## Technical debt register

| ID | Description | REQ risk | Paydown story |
|----|-------------|----------|---------------|
| TD-01 | No rate limiting | REQ-NFR-06 | US-TECH-02 |

Debt is not invisible — link to REQ or accept risk in RAID.

---

## Traceability in monorepo

```
docs/requirements.md     ← source
docs/traceability.md
docs/adr/
packages/*/README.md     ← module → epic map
```

PR checklist: ADR? RTM? REQ in commit?

Next: [Part 19 — Agile solo](19-agile-kanban-scrum-solo.md)
