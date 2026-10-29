# Part 11 — End-to-End Workshop

Do this once with a **real** project idea (2–4 hours). Duplicate the section headings into your project repo.

---

## Scenario

You will build **“StudyBuddy”** — a solo dev tool to log learning sessions and weekly goals. (Replace with your idea; keep structure.)

---

## Step 1: Charter (15 min)

Copy [templates/project-charter.md](../templates/project-charter.md).

Filled example:

- **User:** Self-taught developer studying 5–10 h/week
- **Problem:** No visibility into whether study time matches goals
- **Success (30 days):** Log 20 sessions; complete 4 weekly reviews
- **Non-goals:** Social features, mobile app, AI tutor

---

## Step 2: Goals (10 min)

| ID | Goal | Metric | Target |
|----|------|--------|--------|
| G-1 | Habit visibility | Sessions logged / week | ≥ 3 |
| G-2 | Goal alignment | Weekly review completed | ≥ 75% weeks |

---

## Step 3: MVP scope (15 min)

**In:** log session (topic, duration), weekly goal set, weekly review summary  
**Post-MVP:** charts, tags, export, reminders  
**Won’t:** accounts sync, teams

---

## Step 4: Epics & features (30 min)

| Epic | Features |
|------|----------|
| EP-01 Session logging | F-01-01 Create session, F-01-02 Edit/delete session, F-01-03 List sessions |
| EP-02 Weekly goals | F-02-01 Set weekly hours goal, F-02-02 Progress indicator |
| EP-03 Weekly review | F-03-01 Review prompt, F-03-02 Summary view |

---

## Step 5: Requirements register (30 min)

Sample rows:

| ID | Type | Statement | Priority |
|----|------|-----------|----------|
| REQ-FR-01 | FR | User shall create session with topic, duration ≥ 1 min | Must |
| REQ-FR-02 | FR | User shall view sessions for current week | Must |
| REQ-FR-03 | FR | User shall set weekly hour goal | Must |
| REQ-NFR-01 | NFR | Data persisted locally or DB; no data loss on refresh | Must |
| REQ-NFR-02 | NFR | Core actions complete in ≤ 2 s on mid-range laptop | Should |

---

## Step 6: Stories for EP-01 only (30 min)

**US-01-01:** As a learner, I want to log a session with topic and duration so that I track time spent.

**Acceptance criteria:**

- Given valid topic and duration, when I save, session appears in list with today’s date
- Given duration 0, when I save, show validation error
- Given saved session, when I refresh page, session still listed (REQ-NFR-01)

**Tasks:**

- [ ] Data model + persistence
- [ ] Form UI + validation
- [ ] List view
- [ ] TEST-UNIT-01 duration validation
- [ ] TEST-E2E-01 create + persist

---

## Step 7: RTM starter (15 min)

| Req | Story | Test | Status |
|-----|-------|------|--------|
| REQ-FR-01 | US-01-01 | TEST-E2E-01 | Draft |
| REQ-NFR-01 | US-01-01 | TEST-E2E-01 | Draft |

---

## Step 8: Sprint 1 commitment (10 min)

**Sprint goal:** “User can log and see one week of sessions.”

Stories: US-01-01, US-01-02 (list/filter — write yourself using Part 4)

---

## Step 9: After sprint 1

1. Mark REQ Implemented → Verified when tests pass
2. Retro: was US-01-01 too big?
3. Pull EP-02 stories with same pipeline

---

## Transfer checklist to your project

- [ ] Charter in `docs/charter.md`
- [ ] Requirements in `docs/requirements.md`
- [ ] RTM in `docs/traceability.md`
- [ ] Backlog in GitHub Issues or `docs/backlog.md`
- [ ] ADR folder `docs/adr/`

Next: [Part 12 — Advanced traceability](12-advanced-traceability.md)
