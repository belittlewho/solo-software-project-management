# Part 12 — Advanced Traceability & Change Control

When projects grow (money, users, compliance, collaborators), upgrade RTM and governance.

---

## Multi-level RTM

| Level | Traces |
|-------|--------|
| Business goal | → REQ |
| REQ | → Story |
| Story | → Component / module |
| Component | → Test |
| Test | → Release / build |

**Bidirectional:** any cell links both ways.

---

## Test traceability matrix

Separate table or RTM extension:

| Test ID | Type | Automates REQ | Story | Last run | Result |
|---------|------|---------------|-------|----------|--------|
| TEST-E2E-01 | e2e | REQ-FR-01 | US-01-01 | CI #442 | pass |

**Orphan test policy:** no merge unless TEST links to REQ or marked `TEST-TECH` (infra only).

---

## Change impact analysis

When REQ-FR-12 changes:

1. Search repo for `REQ-FR-12` in RTM, issues, ADRs
2. List affected stories, files, tests
3. Update acceptance criteria before coding
4. Re-run linked tests
5. Bump REQ version in register: `REQ-FR-12 v2`

Change log row:

| Date | REQ | Change | Reason | Author |
|------|-----|--------|--------|--------|

---

## Baselines & releases

**Baseline** = frozen set of REQ IDs at release tag `v1.0.0`.

- Tag git: `v1.0.0`
- Export RTM snapshot: `docs/releases/v1.0.0-rtm.md`

Post-release bugs reference baseline: “Regression vs v1.0.0 REQ-FR-05.”

---

## Compliance-oriented RTM (ISO / audit style)

Auditors ask for:

- Unique requirement IDs
- Approval authority & date
- Verification method per REQ
- Evidence (test report, screenshot, log)

Add columns:

| Approved by | Approval date | Verification evidence |

Solo: you are approver; still **date** the approval.

---

## V-model mapping (learning reference)

```
Requirements ←→ Acceptance tests
Architecture ←→ Integration tests
Design       ←→ Unit tests
Code         ←→ Implementation
```

Not every project needs full V-model; use it when **regulated** or **high risk** (health, finance).

---

## Traceability in CI

Examples:

- PR check: body must reference `REQ-` or `NO-REQ` with reason
- Coverage gate: changed files in `payments/` require tests tagged `REQ-FR-*` checkout
- Generate RTM partial from `@req REQ-FR-01` in test docstrings (custom script)

Start manual; automate when RTM drifts often.

---

## Collaborator handoff

When adding a second person:

1. Onboard via charter + goals + MVP
2. RTM is assignment surface (“pick Verified gaps”)
3. ADRs explain **why** not just **what**
4. Definition of Ready enforced on PRs

---

## Maturity model (self-assessment)

| Level | Behavior |
|-------|----------|
| 0 | Ideas in head; no IDs |
| 1 | Backlog + stories; informal |
| 2 | REQ IDs + RTM-lite + DoD |
| 3 | Full RTM + test links + ADRs |
| 4 | Baselines + change impact + CI checks |

Aim one level above your current pain, not level 4 on day one.

---

## Further reading

- *Software Requirements* (Wiegers) — requirements quality
- *User Story Mapping* (Patton) — journey-first breakdown
- *Shape Up* (Basecamp) — appetite-based scoping
- IEEE 29148 — requirement standard (reference, not mandatory reading)

---

You now have a full path: **charter → reqs → epics → stories → tasks → RTM → rhythm → advanced governance.**

Return to [README](../README.md) for templates and quick reference.
