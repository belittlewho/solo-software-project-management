# Part 19 — Agile, Kanban & Scrum (Team of One)

You can use industry frameworks **without** fake standups with yourself. Keep the **intent**, shrink the **ceremony**.

---

## Waterfall vs iterative (solo)

| Waterfall habit | Solo iterative replacement |
|-----------------|----------------------------|
| Write all specs upfront | Charter + MVP REQs; refine weekly |
| Big bang release | Walking skeleton early |
| Change = failure | Change = update REQ + RTM |
| Phase gates | Milestones with exit criteria |

Even “waterfall” documents (SRS) can live in git with **versioned** updates.

---

## Scrum mapped to solo

| Scrum | Solo adaptation |
|-------|-----------------|
| Product Owner | You (wear “outcome hat”) |
| Developer | You (wear “implementation hat”) |
| Sprint | 1–2 weeks fixed |
| Sprint planning | Monday: pick 1–3 outcomes |
| Daily scrum | 3-line written log (optional) |
| Sprint review | Friday demo to screen/recording |
| Retrospective | 15 min: one process fix |
| Product backlog | GitHub Issues + priority |
| Sprint backlog | Milestone or “Sprint 12” label |
| Increment | Potentially shippable on main |

**Tip:** In planning, ask “PO me”: *Is this Must for MVP?* Then “Dev me”: *Can I finish in sprint?*

---

## Kanban mapped to solo

Columns: **Inbox → Ready → Doing (WIP 2) → Review → Done**

Policies written on board:

- Ready = DoR satisfied  
- Doing max 2 cards  
- Review = PR open + tests  
- Done = DoD + RTM updated  

Kanban fits **continuous** flow; Scrum fits **deadline cadence**. Pick one primary; many solos blend (2-week cadence + WIP limits).

---

## Estimation in agile

See [Part 24](24-estimation-planning-milestones.md). Use points for **velocity learning**, not promises to stakeholders.

---

## Velocity (solo)

Track points completed per sprint. After 3 sprints:

- Average velocity → sprint capacity  
- If committed >> delivered, stories too big or scope creep  

---

## Ceremonies you can skip

- Sprint burndown charts (optional if weekly retro honest)  
- Formal PO approval meetings  
- Cross-team PI planning  

---

## Ceremonies you must not skip

- Weekly replan (backlog order changes)  
- Definition of Done before marking Verified  
- RTM update when merging behavior changes  

Next: [Part 20 — Release & DevOps](20-release-devops-operations.md)
