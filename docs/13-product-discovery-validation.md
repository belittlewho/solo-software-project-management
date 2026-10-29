# Part 13 — Product Discovery & Validation

Before REQ-FR-01 exists, you need evidence the **problem is real** and your **MVP hypothesis** is worth building.

---

## Discovery vs delivery

| Discovery | Delivery |
|-----------|----------|
| Should we build this? | Build the right thing correctly |
| Cheap experiments | Implementation |
| Throwaway prototypes | Maintained code |
| Charter, interviews | RTM, sprints |

Spend **10–30%** of early project time in discovery; saves months of wrong code.

---

## Problem validation checklist

- [ ] Named **one** primary user (not “everyone”)
- [ ] User can describe pain in their words (you quoted them)
- [ ] They already pay or struggle (time/money) for a workaround
- [ ] You can reach 5 such people in 2 weeks
- [ ] Success metric is measurable without your app (baseline)

If ≥3 fail, do not write requirements yet — refine problem.

---

## Solution validation (before MVP code)

| Method | Effort | What you learn |
|--------|--------|----------------|
| **Problem interview** | 30 min × 5 | Pain, workflow, alternatives |
| **Solution interview** | 30 min × 5 | Reaction to mock, not code |
| **Landing page + waitlist** | 1 day | Interest signal |
| **Concierge MVP** | 1 week | Manual service before automation |
| **Wizard of Oz** | days | User thinks software works; you manual backend |
| **Prototype (Figma / HTML)** | days | Usability, scope shrink |

Document findings in `docs/discovery-notes.md` with date and source.

---

## Interview script (minimal)

1. Tell me about the last time you [problem context].
2. What did you do? What was frustrating?
3. What tools did you try? What failed?
4. If you had a magic wand, what would change?
5. (Show mock) What would you use this for? What’s missing?

Do **not** pitch your idea first — listen first.

---

## Hypothesis template

```markdown
We believe that **[user]** experiences **[problem]**
When **[situation]**, they **[current behavior]**.
If we deliver **[MVP capability]**, they will **[behavior change]**
We will know we are right when **[metric]** reaches **[target]** by **[date]**.
```

Link hypothesis to goals G-1 in charter.

---

## When to stop discovering and start REQ IDs

Start the requirements register when:

- Problem validated (or you accept personal-project risk)
- MVP boundary is one sentence
- You can name 3 capabilities for MVP

Continue lightweight discovery in parallel for **post-MVP** only.

---

## Pivot log

| Date | What we learned | Decision |
|------|-----------------|----------|
| | Users don’t want X | Remove EP-03 from MVP |

Pivots update charter, non-goals, and deprecate REQ IDs (never silent delete).

Next: [Part 14 — Document types](14-document-types-and-artifacts.md)
