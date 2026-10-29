# Part 27 — Visual Maps Reference (Mermaid)

Copy-paste into your repo `docs/diagrams/`.

---

## Artifact dependency (study order)

```mermaid
flowchart LR
  Charter --> REQ
  REQ --> RTM
  REQ --> Stories
  Stories --> Tests
  Tests --> RTM
  ADR --> RTM
```

---

## Decomposition ladder

```mermaid
flowchart TB
  Vision --> Goals
  Goals --> MVP
  MVP --> Epics
  Epics --> Features
  Features --> Stories
  Stories --> Tasks
  REQ --> RTM
  Stories --> RTM
  Tasks --> Code
  Code --> RTM
```

---

## Prioritization flow

```mermaid
flowchart TD
  Idea --> Inbox
  Inbox --> Refine{DoR?}
  Refine -->|no| Inbox
  Refine -->|yes| Backlog
  Backlog --> MoSCoW
  MoSCoW --> Sprint
  Sprint --> Done{DoD?}
  Done -->|no| Sprint
  Done -->|yes| Verified
```

---

## Release pipeline

```mermaid
flowchart LR
  Dev --> CI
  CI --> Staging
  Staging --> Smoke
  Smoke --> Prod
  Prod --> Monitor
```

Use diagrams in PRD appendix for onboarding collaborators.

Next: [FAQ & cheat sheet](99-faq-antipatterns-cheatsheet.md)
