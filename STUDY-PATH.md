# Complete study path (no knowledge gaps)

Read in this order. Each part lists **prerequisites** and **you will know** outcomes. Skip nothing on first pass; use the index later for reference.

---

## Phase A — Thinking before tickets (Days 1–2)

| Order | Part | File | You will know |
|-------|------|------|----------------|
| A0 | Glossary & map of all artifacts | [docs/00-glossary-and-map.md](docs/00-glossary-and-map.md) | Every term and how artifacts connect |
| A1 | Foundations | [docs/01-foundations.md](docs/01-foundations.md) | Outcome vs output; vertical slices |
| A2 | Product discovery & validation | [docs/13-product-discovery-validation.md](docs/13-product-discovery-validation.md) | Problem/solution fit before REQ IDs |
| A3 | Personas, JTBD, journeys | [docs/15-personas-jtbd-user-journeys.md](docs/15-personas-jtbd-user-journeys.md) | Who you build for; journey → requirements |
| A4 | Document types (PRD, SRS, ADR…) | [docs/14-document-types-and-artifacts.md](docs/14-document-types-and-artifacts.md) | Which doc to write when |

**Checkpoint:** You can fill [templates/project-charter.md](templates/project-charter.md) and one persona without opening your IDE.

---

## Phase B — Decomposition (Days 3–5)

| Order | Part | File | You will know |
|-------|------|------|----------------|
| B1 | Decomposition ladder | [docs/02-decomposition-ladder.md](docs/02-decomposition-ladder.md) | Vision → tasks |
| B2 | Use cases & simple diagrams | [docs/16-use-cases-and-diagrams.md](docs/16-use-cases-and-diagrams.md) | Actors, flows, context |
| B3 | Event storming & domain nouns | [docs/26-event-storming-domain-decomposition.md](docs/26-event-storming-domain-decomposition.md) | Modules from domain events |
| B4 | Writing requirements | [docs/03-writing-requirements.md](docs/03-writing-requirements.md) | FR, NFR, BR, CON with IDs |
| B5 | User stories & AC | [docs/04-user-stories-acceptance-criteria.md](docs/04-user-stories-acceptance-criteria.md) | INVEST, Gherkin |
| B6 | Modules & WBS | [docs/05-modules-and-wbs.md](docs/05-modules-and-wbs.md) | Technical tree + dependencies |
| B7 | Prioritization | [docs/06-prioritization.md](docs/06-prioritization.md) | MoSCoW, RICE, walking skeleton |

**Checkpoint:** MVP epics, ≥10 REQ IDs, ≥5 stories with acceptance criteria, [templates/feature-breakdown.md](templates/feature-breakdown.md) filled.

---

## Phase C — Traceability & quality (Days 6–7)

| Order | Part | File | You will know |
|-------|------|------|----------------|
| C1 | RTM basics | [docs/07-traceability-matrix.md](docs/07-traceability-matrix.md) | Forward/backward trace |
| C2 | Testing & verification | [docs/17-testing-quality-verification.md](docs/17-testing-quality-verification.md) | Test pyramid linked to REQ |
| C3 | Architecture & design trace | [docs/18-architecture-design-traceability.md](docs/18-architecture-design-traceability.md) | ADR, C4-lite, API contracts |
| C4 | NFR catalog (security, perf…) | [docs/21-security-privacy-compliance-nfr-catalog.md](docs/21-security-privacy-compliance-nfr-catalog.md) | NFRs you would otherwise forget |
| C5 | Advanced RTM | [docs/12-advanced-traceability.md](docs/12-advanced-traceability.md) | Change impact, baselines |

**Checkpoint:** [templates/traceability-matrix.md](templates/traceability-matrix.md) with every Must REQ linked to ≥1 test or explicit manual verification.

---

## Phase D — Delivery & operations (Days 8–9)

| Order | Part | File | You will know |
|-------|------|------|----------------|
| D1 | Backlog & DoD | [docs/08-backlog-and-dod.md](docs/08-backlog-and-dod.md) | Ready/Done definitions |
| D2 | Estimation & milestones | [docs/24-estimation-planning-milestones.md](docs/24-estimation-planning-milestones.md) | Points, buffers, critical path |
| D3 | Agile / Kanban / Scrum (solo) | [docs/19-agile-kanban-scrum-solo.md](docs/19-agile-kanban-scrum-solo.md) | Ceremonies that survive team size = 1 |
| D4 | Roadmaps & OKRs | [docs/25-roadmaps-okrs-themes.md](docs/25-roadmaps-okrs-themes.md) | Themes vs backlog vs roadmap |
| D5 | Risks & dependencies | [docs/09-risks-assumptions-dependencies.md](docs/09-risks-assumptions-dependencies.md) | RAID, spikes, ADR |
| D6 | Release & DevOps | [docs/20-release-devops-operations.md](docs/20-release-devops-operations.md) | Environments, rollback, runbooks |
| D7 | Solo rhythm | [docs/10-solo-execution-rhythm.md](docs/10-solo-execution-rhythm.md) | Weekly loop |

**Checkpoint:** One milestone with exit criteria; [templates/raid-log.md](templates/raid-log.md); release checklist draft.

---

## Phase E — Practice & reference (Day 10+)

| Order | Part | File | You will know |
|-------|------|------|----------------|
| E1 | End-to-end workshop | [docs/11-end-to-end-workshop.md](docs/11-end-to-end-workshop.md) | Full pipeline once |
| E2 | Tooling (GitHub Issues…) | [docs/23-tooling-github-linear-notion.md](docs/23-tooling-github-linear-notion.md) | IDs in your tracker |
| E3 | Stakeholders & communication | [docs/22-stakeholders-communication.md](docs/22-stakeholders-communication.md) | Updates, scope conversations |
| E4 | Visual maps | [docs/27-visual-maps-reference.md](docs/27-visual-maps-reference.md) | Mermaid templates |
| E5 | FAQ & anti-patterns | [docs/99-faq-antipatterns-cheatsheet.md](docs/99-faq-antipatterns-cheatsheet.md) | Quick rescue |

**Checkpoint:** Repeat workshop on **your** production idea; open issues tagged with `REQ-FR-*`.

---

## Concept coverage matrix (nothing left out)

| Topic | Where covered |
|-------|----------------|
| Idea → charter | 13, 14, templates/charter |
| Validation / interviews | 13 |
| Personas / JTBD | 15 |
| User journeys | 15, 16 |
| Use cases | 16 |
| Context / C4 diagrams | 18, 27 |
| Event storming | 26 |
| FR / NFR / business rules | 03, 21 |
| Epics / features / stories / tasks | 02, 04, 08 |
| INVEST / Gherkin | 04 |
| WBS / modules / DDD-lite | 05, 26 |
| MoSCoW / RICE / slicing | 06 |
| RTM / traceability | 07, 12, 17, 18 |
| Test pyramid / QA | 17 |
| ADR / API design | 18 |
| Backlog / DoR / DoD | 08 |
| Story points / estimation | 24 |
| Sprints / Kanban | 19 |
| Roadmap / OKR | 25 |
| RAID / spikes | 09 |
| Release / CI / monitoring | 20 |
| Security / privacy NFRs | 21 |
| GitHub Issues workflow | 23 |
| Stakeholder comms | 22 |
| Waterfall vs agile (solo) | 19, 99 |
| Compliance / audit RTM | 12, 21 |
| Maintenance / tech debt | 99, 20 |

If you find a topic not in this table, open an issue on the repo — treat that as a gap to close.
