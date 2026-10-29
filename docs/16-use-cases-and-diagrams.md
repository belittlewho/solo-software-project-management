# Part 16 — Use Cases & Diagrams

Use cases complement user stories: better for **complex flows**, **multiple actors**, and **alternate paths**.

---

## When to use use case vs user story

| Use case | User story |
|----------|------------|
| Multi-step workflow | Single testable slice |
| Several actors | One primary role |
| Many alternate flows | Happy path + few errors |
| Regulated domains | Agile delivery unit |

Often: **one use case** → **many stories**.

Template: [templates/use-case.md](../templates/use-case.md)

---

## Use case structure

- **ID:** UC-01  
- **Name:** Place order  
- **Primary actor:** Buyer  
- **Preconditions:** Logged in, cart non-empty  
- **Postconditions:** Order created, payment captured  
- **Main success scenario:** numbered steps  
- **Extensions:** 3a payment fails, 3b out of stock  

Link UC-01 to REQ-FR-* in register.

---

## Context diagram (system boundary)

```mermaid
flowchart LR
  User[Buyer]
  Admin[Admin]
  Sys[Your system]
  Pay[Payment provider]
  Email[Email service]
  User --> Sys
  Admin --> Sys
  Sys --> Pay
  Sys --> Email
```

External systems → **dependencies** in RAID and **constraints** (REQ-CON).

---

## Container diagram (C4 level 2 — lite)

```mermaid
flowchart TB
  subgraph system [Your product]
    Web[Web app]
    API[API]
    DB[(Database)]
  end
  User --> Web
  Web --> API
  API --> DB
  API --> Pay[Stripe]
```

Each box can become a **module** in WBS (Part 5).

---

## Sequence diagram (one happy path)

Use for ambiguous API flows before coding.

```mermaid
sequenceDiagram
  participant U as User
  participant W as Web
  participant A as API
  participant P as Payment
  U->>W: Checkout
  W->>A: POST /orders
  A->>P: Create intent
  P-->>A: client_secret
  A-->>W: order_id
  W-->>U: Show payment UI
```

Sequence → **tasks** under story; messages → **API requirements**.

---

## State machine (entity lifecycle)

For Order, Subscription, Invoice:

```mermaid
stateDiagram-v2
  [*] --> Draft
  Draft --> PendingPayment: submit
  PendingPayment --> Paid: capture
  PendingPayment --> Draft: cancel
  Paid --> Fulfilled: ship
```

Each transition → **REQ-FR** or **REQ-BR**; invalid transitions → validation stories.

---

## Activity diagram (decision-heavy)

Use when many branches (approval workflows). Mermaid `flowchart` with diamonds for decisions.

---

## Diagram → RTM

Add RTM column or footnote: **Design ref:** UC-02, diagram in `docs/diagrams/checkout.md`.

Next: [Part 17 — Testing & verification](17-testing-quality-verification.md)
