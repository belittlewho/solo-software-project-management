# Part 26 — Event Storming & Domain Decomposition

When nouns are tangled, **domain events** reveal modules and stories faster than screen mockups.

---

## Event storming (solo, 90 min)

Materials: paper or Miro, orange = event, blue = command, yellow = aggregate, pink = external system.

**Steps:**

1. Write **domain events** past tense: `OrderPlaced`, `PaymentFailed`, `InvoiceSent`  
2. Order events in timeline per persona journey  
3. Add **commands** that cause events: `PlaceOrder` → `OrderPlaced`  
4. Group events around **aggregates** (Order, Payment, Invoice)  
5. Draw boundaries — high interaction inside, low across  

Each aggregate → candidate **module** (Part 5).

---

## From event to story

| Event | Story angle |
|-------|-------------|
| PaymentFailed | User sees retry + cart preserved |
| InvoiceSent | User receives PDF link email |

Events become AC or integration test scenarios.

---

## Ubiquitous language

Write glossary `docs/domain-glossary.md`:

| Term | Definition | Not |
|------|------------|-----|
| Order | Buyer commitment to purchase | Shipment |

Same term in REQ, code, and UI — reduces breakdown errors.

---

## Bounded context signals

Split modules when:

- Same word means different things (Admin “customer” vs CRM “customer”)  
- Different lifecycles collide in one table  

Integrate via API/events, not shared tables.

---

## Event → RTM

Optional column **Domain event** for backend-heavy systems.

Next: [Part 27 — Visual maps](27-visual-maps-reference.md)
