# Solo Software Project Management & Requirements Breakdown

**Complete path from idea → requirements → modules → traceability → release** — for software engineers who code well but struggle to decompose and document work.

No intentional gaps: follow **[STUDY-PATH.md](STUDY-PATH.md)** for ordered reading and a [concept coverage matrix](STUDY-PATH.md#concept-coverage-matrix-nothing-left-out).

---

## Start here

| If you… | Open |
|---------|------|
| Want zero jargon gaps first | [Part 0 — Glossary & map](docs/00-glossary-and-map.md) |
| Need the full curriculum in order | [STUDY-PATH.md](STUDY-PATH.md) |
| Want to practice once end-to-end | [Part 11 — Workshop](docs/11-end-to-end-workshop.md) |
| Need a rescue one-pager | [Part 99 — FAQ & cheat sheet](docs/99-faq-antipatterns-cheatsheet.md) |

---

## Full table of contents

### Core path (original)

| Part | Topic | File |
|------|--------|------|
| 0 | Glossary & artifact map | [docs/00-glossary-and-map.md](docs/00-glossary-and-map.md) |
| 1 | Foundations | [docs/01-foundations.md](docs/01-foundations.md) |
| 2 | Decomposition ladder | [docs/02-decomposition-ladder.md](docs/02-decomposition-ladder.md) |
| 3 | Writing requirements | [docs/03-writing-requirements.md](docs/03-writing-requirements.md) |
| 4 | User stories & AC | [docs/04-user-stories-acceptance-criteria.md](docs/04-user-stories-acceptance-criteria.md) |
| 5 | Modules & WBS | [docs/05-modules-and-wbs.md](docs/05-modules-and-wbs.md) |
| 6 | Prioritization | [docs/06-prioritization.md](docs/06-prioritization.md) |
| 7 | Traceability matrix | [docs/07-traceability-matrix.md](docs/07-traceability-matrix.md) |
| 8 | Backlog & DoD | [docs/08-backlog-and-dod.md](docs/08-backlog-and-dod.md) |
| 9 | Risks & dependencies | [docs/09-risks-assumptions-dependencies.md](docs/09-risks-assumptions-dependencies.md) |
| 10 | Solo execution rhythm | [docs/10-solo-execution-rhythm.md](docs/10-solo-execution-rhythm.md) |
| 11 | End-to-end workshop | [docs/11-end-to-end-workshop.md](docs/11-end-to-end-workshop.md) |
| 12 | Advanced traceability | [docs/12-advanced-traceability.md](docs/12-advanced-traceability.md) |

### Extended path (closes knowledge gaps)

| Part | Topic | File |
|------|--------|------|
| 13 | Product discovery & validation | [docs/13-product-discovery-validation.md](docs/13-product-discovery-validation.md) |
| 14 | Document types (PRD, SRS, ADR…) | [docs/14-document-types-and-artifacts.md](docs/14-document-types-and-artifacts.md) |
| 15 | Personas, JTBD, journeys | [docs/15-personas-jtbd-user-journeys.md](docs/15-personas-jtbd-user-journeys.md) |
| 16 | Use cases & diagrams | [docs/16-use-cases-and-diagrams.md](docs/16-use-cases-and-diagrams.md) |
| 17 | Testing & verification | [docs/17-testing-quality-verification.md](docs/17-testing-quality-verification.md) |
| 18 | Architecture & design trace | [docs/18-architecture-design-traceability.md](docs/18-architecture-design-traceability.md) |
| 19 | Agile / Kanban / Scrum (solo) | [docs/19-agile-kanban-scrum-solo.md](docs/19-agile-kanban-scrum-solo.md) |
| 20 | Release & DevOps | [docs/20-release-devops-operations.md](docs/20-release-devops-operations.md) |
| 21 | Security & NFR catalog | [docs/21-security-privacy-compliance-nfr-catalog.md](docs/21-security-privacy-compliance-nfr-catalog.md) |
| 22 | Stakeholders & communication | [docs/22-stakeholders-communication.md](docs/22-stakeholders-communication.md) |
| 23 | Tooling (GitHub Issues…) | [docs/23-tooling-github-linear-notion.md](docs/23-tooling-github-linear-notion.md) |
| 24 | Estimation & milestones | [docs/24-estimation-planning-milestones.md](docs/24-estimation-planning-milestones.md) |
| 25 | Roadmaps & OKRs | [docs/25-roadmaps-okrs-themes.md](docs/25-roadmaps-okrs-themes.md) |
| 26 | Event storming & domain | [docs/26-event-storming-domain-decomposition.md](docs/26-event-storming-domain-decomposition.md) |
| 27 | Visual maps (Mermaid) | [docs/27-visual-maps-reference.md](docs/27-visual-maps-reference.md) |
| 99 | FAQ, anti-patterns, cheat sheet | [docs/99-faq-antipatterns-cheatsheet.md](docs/99-faq-antipatterns-cheatsheet.md) |

---

## Templates

| Template | Purpose |
|----------|---------|
| [project-charter.md](templates/project-charter.md) | Why, who, success, non-goals |
| [prd-lite.md](templates/prd-lite.md) | Product requirements overview |
| [user-persona.md](templates/user-persona.md) | Persona + JTBD |
| [requirements-register.md](templates/requirements-register.md) | REQ-* register (your SRS) |
| [use-case.md](templates/use-case.md) | Actors & flows |
| [feature-breakdown.md](templates/feature-breakdown.md) | Epic → feature → story tree |
| [traceability-matrix.md](templates/traceability-matrix.md) | RTM |
| [test-plan-lite.md](templates/test-plan-lite.md) | Release verification |
| [raid-log.md](templates/raid-log.md) | Risks, assumptions, issues, deps |
| [sprint-backlog.md](templates/sprint-backlog.md) | Sprint commitment |
| [weekly-planning.md](templates/weekly-planning.md) | Weekly loop |

GitHub issue template for stories: [.github/ISSUE_TEMPLATE/story.yml](.github/ISSUE_TEMPLATE/story.yml)

---

## Quick reference: decomposition chain

1. **Who** + JTBD  
2. **Outcome** + metric  
3. **MVP** + non-goals  
4. **Capabilities** (epics)  
5. **Features** → **stories** + acceptance criteria  
6. **REQ IDs** + **RTM** + **tests**  
7. **Tasks** (≤ 1 day)

---

## License

MIT — use, fork, and adapt freely.
