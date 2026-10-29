# Solo Software Project Management & Requirements Breakdown

**Learn from scratch to advanced:** how to turn a vague product idea into modules, features, and shippable work — including traceability matrices, acceptance criteria, and solo-friendly rituals.

Written for software engineers who can code but struggle to **decompose** and **document** what they are building.

---

## How to use these notes

1. Read **[Part 1 — Foundations](docs/01-foundations.md)** if breakdown feels impossible or overwhelming.
2. Work through **[Part 2 — The decomposition ladder](docs/02-decomposition-ladder.md)** with your real project beside you.
3. Copy templates from **[templates/](templates/)** into your repo or Notion.
4. Do the **[Part 11 — End-to-end workshop](docs/11-end-to-end-workshop.md)** once on a small idea, then repeat on your main project.
5. Add **[Part 12 — Advanced traceability](docs/12-advanced-traceability.md)** when you need audit trails, testing discipline, or compliance-style rigor.

---

## Table of contents

| Part | Topic | File |
|------|--------|------|
| 1 | Why engineers struggle & mental models | [docs/01-foundations.md](docs/01-foundations.md) |
| 2 | Vision → MVP → epics → features → stories → tasks | [docs/02-decomposition-ladder.md](docs/02-decomposition-ladder.md) |
| 3 | Writing requirements (functional, NFR, constraints) | [docs/03-writing-requirements.md](docs/03-writing-requirements.md) |
| 4 | User stories & acceptance criteria (Gherkin) | [docs/04-user-stories-acceptance-criteria.md](docs/04-user-stories-acceptance-criteria.md) |
| 5 | Modules, bounded contexts & technical WBS | [docs/05-modules-and-wbs.md](docs/05-modules-and-wbs.md) |
| 6 | Prioritization (MoSCoW, RICE, slicing) | [docs/06-prioritization.md](docs/06-prioritization.md) |
| 7 | Traceability matrix (RTM) — basics | [docs/07-traceability-matrix.md](docs/07-traceability-matrix.md) |
| 8 | Backlog, milestones & Definition of Done | [docs/08-backlog-and-dod.md](docs/08-backlog-and-dod.md) |
| 9 | Risk, assumptions, dependencies | [docs/09-risks-assumptions-dependencies.md](docs/09-risks-assumptions-dependencies.md) |
| 10 | Solo execution rhythm (weekly loop) | [docs/10-solo-execution-rhythm.md](docs/10-solo-execution-rhythm.md) |
| 11 | **Workshop:** idea → RTM → sprint 1 | [docs/11-end-to-end-workshop.md](docs/11-end-to-end-workshop.md) |
| 12 | Advanced RTM, test traceability, change impact | [docs/12-advanced-traceability.md](docs/12-advanced-traceability.md) |

---

## Templates

| Template | Purpose |
|----------|---------|
| [project-charter.md](templates/project-charter.md) | One-page “why, who, success, non-goals” |
| [requirements-register.md](templates/requirements-register.md) | Numbered requirements with IDs |
| [traceability-matrix.md](templates/traceability-matrix.md) | Req → design → code → test links |
| [feature-breakdown.md](templates/feature-breakdown.md) | Epic/feature/story tree |
| [weekly-planning.md](templates/weekly-planning.md) | Solo weekly plan + retro |

---

## Quick reference: the decomposition question chain

Ask these in order whenever you feel stuck:

1. **Who** is the user and **what job** are they hiring this product to do?
2. **What outcome** proves the product works (metric or observable behavior)?
3. **What is MVP** — the smallest slice that delivers that outcome?
4. **What capabilities** must exist for MVP (verbs: “sign up”, “pay”, “search”)?
5. **For each capability**, what are **3–7 user-visible **features**?
6. **For each feature**, what **stories** with **acceptance criteria**?
7. **For each story**, what **tasks** (≤ 1 day each)?

If a “task” is bigger than a day, it is still a story or feature — split again.

---

## License

MIT — use, fork, and adapt freely.
