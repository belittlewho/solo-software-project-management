# Part 23 — Tooling: GitHub Issues, Linear, Notion

Traceability fails when tools diverge. Pick a **tracker** and mirror **REQ IDs** from git.

---

## Recommended solo stack (free tier friendly)

| Layer | Tool | Holds |
|-------|------|-------|
| Truth for REQ text | Git `docs/requirements.md` | Wording, status |
| Truth for RTM | Git `docs/traceability.md` | Links |
| Execution | GitHub Issues | Stories, tasks |
| Design | Figma + link in issue | |
| CI | GitHub Actions | TEST-* |

---

## GitHub Issues conventions

**Labels:**

- `type:story`, `type:bug`, `type:spike`  
- `priority:must`, `priority:should`  
- `epic:EP-02`  
- `req:FR-12` (one primary per issue; extras in body)

**Issue title:** `[US-02-03] Buyer pays with Mobile Money`

**Body template:**

```markdown
## User story
As a …

## Acceptance criteria
- [ ] …

## Requirements
- REQ-FR-08
- REQ-NFR-SEC-07

## RTM
- [ ] Updated on merge

## Tasks
- [ ] …
```

**Milestones:** `M1 MVP`, `Sprint 2026-W44`

**Projects (v2):** Columns Ready / Doing / Done with WIP optional.

---

## Linking PRs

PR title: `feat(checkout): mobile money [REQ-FR-08]`

PR body:

```markdown
Closes #42
## Traceability
- REQ: REQ-FR-08, REQ-NFR-SEC-07
- Tests: TEST-E2E-04
- RTM: updated
```

Use `Closes #` for auto-close; RTM still manual unless scripted.

---

## Linear / Jira (if you use them)

Custom field **Requirement ID** required on stories.  
Sync rule: export REQ register weekly or use API — **git wins** on conflict.

---

## Notion

Good for discovery notes, persona gallery.  
**Do not** let Notion be only copy of REQs — duplicate drift guaranteed.  
Embed link to GitHub `docs/requirements.md` raw or rendered.

---

## Automation ideas (later)

- GitHub Action: PR must mention `REQ-` or `NO-REQ:` reason  
- Script: parse `REQ-FR-\d+` from tests → partial RTM report  

Start manual until pain justifies automation.

Next: [Part 24 — Estimation](24-estimation-planning-milestones.md)
