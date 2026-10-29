# Part 2 — The Decomposition Ladder

Use this ladder every time. **Do not skip rungs.** Each level answers one question.

---

## Rung 0: Idea (messy)

“I want to build X for Y.” Keep it messy in a scratch pad.

---

## Rung 1: Problem & vision (1 paragraph)

**Template:**

> For **[primary user]**, who **[situation / pain]**, **[product name]** is a **[category]** that **[key benefit]**. Unlike **[alternative]**, we **[differentiator]**.

If you cannot name the primary user, stop and pick one persona only.

---

## Rung 2: Goals & success metrics

| Goal ID | Goal | Metric | Target | Timeframe |
|---------|------|--------|--------|-----------|
| G-1 | … | … | … | … |

Examples:

- G-1: Validate willingness to pay — Conversion checkout started → paid ≥ 2% — 90 days
- G-2: Reduce support load — Password reset self-serve ≥ 80% — 60 days

Every epic should trace to at least one goal.

---

## Rung 3: MVP boundary

**MVP hypothesis:** “If we deliver **[capability A + B]**, **[user]** will **[behavior]** leading to **[metric]**.”

List:

- **In MVP:** bullet list (≤ 7 items)
- **Post-MVP:** parking lot
- **Non-goals:** what you refuse to build in this phase

Rule: MVP should be embarrassingly small but **demonstrable to a real user**.

---

## Rung 4: Capabilities (epics)

Capabilities are **verbs at product level**, not screens.

Example for a marketplace MVP:

| Epic ID | Capability | Maps to goals |
|---------|------------|---------------|
| EP-01 | Browse catalog | G-1 |
| EP-02 | Checkout & pay | G-1 |
| EP-03 | Seller lists product | G-1 |

Each epic gets a one-line **outcome statement**.

---

## Rung 5: Features

A **feature** is a user-visible chunk inside an epic.

**Decomposition technique: CRUD + lifecycle + exceptions**

For entity “Order”:

- Create (place order)
- Read (order history, detail)
- Update (cancel before ship — maybe post-MVP)
- Delete (rare; often “archive”)
- Lifecycle (draft → paid → fulfilled)
- Exceptions (payment failed, out of stock)

For “Authentication”:

- Register, login, logout, reset password, session expiry, OAuth (maybe later)

**Feature ID convention:** `F-{EPIC}-{nn}` e.g. `F-02-03 Mobile Money checkout`.

---

## Rung 6: User stories

Format:

> As a **\<role\>**, I want **\<capability\>**, so that **\<benefit\>**.

Rules:

- One story = one testable behavior slice
- If “and” appears twice in the title, split it
- Roles come from your persona list (keep ≤ 3 for MVP)

**Story ID:** `US-{feature}-{nn}` or tool-native (#123).

---

## Rung 7: Acceptance criteria

Each story needs **observable** criteria (see Part 4). Without them, “done” is undefined.

---

## Rung 8: Tasks

Tasks are for **you the implementer**:

- Add migration for `orders` table
- Wire Stripe webhook handler
- Add e2e test for happy path

**Task sizing:** If > 1 day, split. If < 30 minutes, batch into a “implementation task group” under the story.

---

## The “5 Whys” for stuck breakdown

When you cannot split a feature:

1. Why does the user need this? → reveals outcome
2. Why now (MVP)? → may defer
3. Why is this one block? → find subprocesses
4. Why would this fail? → exception stories
5. Why is this the same as that? → merge duplicates

---

## Worked mini-example

**Idea:** “App for freelancers to track invoices.”

| Level | Example |
|-------|---------|
| MVP | Create invoice, send PDF link, mark paid |
| Epic EP-01 | Invoice management |
| Feature F-01-01 | Create draft invoice |
| Story US-01-01 | As a freelancer, I want line items with qty/rate so totals compute automatically |
| AC | Given 2 line items, when I save, total = sum(qty×rate); tax field optional |
| Tasks | Schema, API, UI form, unit test for total |

---

## Checklist before you code

- [ ] MVP ≤ 7 capabilities
- [ ] Every MVP story has acceptance criteria
- [ ] Requirements have IDs (REQ-xxx)
- [ ] RTM started (even 5 rows)
- [ ] Post-MVP list written (so you do not “accidentally” build it)

Next: [Part 3 — Writing requirements](03-writing-requirements.md)
