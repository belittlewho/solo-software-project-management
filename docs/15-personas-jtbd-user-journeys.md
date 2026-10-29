# Part 15 — Personas, JTBD & User Journeys

Breakdown fails when “user” is abstract. These tools make **who** and **when** concrete.

---

## Persona (one page)

Template: [templates/user-persona.md](../templates/user-persona.md)

Include:

- Name (fictional), role, environment  
- Goals (jobs)  
- Frustrations  
- Technical comfort  
- **Quote** in their voice  

MVP: **one primary persona**. Secondary personas are post-MVP unless B2B with buyer vs user.

---

## Jobs To Be Done (JTBD)

Format:

> When **[situation]**, I want to **[motivation]**, so I can **[expected outcome]**.

Example:

> When **I finish a study session**, I want to **log topic and duration in under 30 seconds**, so I can **see if I’m on track for the week**.

Each JTBD spawns **1–3 epics**. Map JTBD → REQ → stories in RTM notes column.

---

## User journey map

Rows: **Phases** (Discover → Decide → Use → Support → Return)  
Columns: **Actions**, **Thoughts**, **Pain**, **Opportunities**

| Phase | Action | Pain | Opportunity (feature) |
|-------|--------|------|------------------------|
| Onboard | Sign up | Long form | Social login (Could) |
| Core | Create invoice | Tax math | Auto-calculate (Must) |

**Opportunity** column feeds epics; **Pain** validates discovery.

---

## Story mapping (Jeff Patton)

Horizontal axis = **time / journey order**  
Vertical = **details** (top = MVP walking skeleton, bottom = enhancements)

```
        Walk skeleton ──────────────────────────────►
        │ login │ catalog │ cart │ pay │ confirm │
        v2    │ filters │ wishlist │ ...
        v3    │ reviews │ recommendations │ ...
```

Cut **horizontal line** for MVP: everything above line ships first.

---

## From journey to requirements

For each journey step:

1. Actor (persona)  
2. Trigger  
3. System response (→ FR)  
4. Failure modes (→ stories + AC)  
5. Quality (→ NFR: speed, accessibility)

Example step “Pay” → REQ-FR-08, REQ-NFR-02 (PCI), REQ-BR-03 (refund rule).

---

## Empathy map (optional)

| Says | Thinks | Does | Feels |
|------|--------|------|-------|
| | | | |

Use before writing marketing copy; secondary for breakdown.

Next: [Part 16 — Use cases & diagrams](16-use-cases-and-diagrams.md)
