# Part 10 — Solo Execution Rhythm

Process only works if it fits a **weekly calendar**.

---

## Recommended cadence

| When | Activity | Duration |
|------|----------|----------|
| Sunday or Monday | Planning + pull sprint | 45–60 min |
| Daily (optional) | Standup note (async) | 5 min |
| Mid-week | Scope check / cut | 15 min |
| Friday | Demo + retro + RTM update | 30 min |

---

## Monday planning script

1. Review goals G-1, G-2 — still right?
2. Pick **1–3 outcomes** for the week (not 10 tasks)
3. Pull stories from backlog; confirm DoR
4. Note risks from RAID log
5. Block calendar for deep work (2–4 h blocks)

Use [templates/weekly-planning.md](../templates/weekly-planning.md).

---

## Daily standup (written, solo)

Three lines in a log file:

```markdown
## 2026-10-29
- Yesterday: …
- Today: …
- Blocked: … (REQ / story ID)
```

Blocked > 2 days → shrink scope, spike, or ask for help.

---

## Friday retro (keep it tiny)

```markdown
- Shipped: US-…
- Slipped: because …
- One change next week: …
```

Improve **system**, not willpower (“split stories smaller” beats “try harder”).

---

## Metrics dashboard (markdown)

`docs/metrics.md` updated weekly:

| Week | Stories done | Must REQ verified | Cycle time (median) | Notes |
|------|--------------|-------------------|---------------------|-------|

Cycle time = story start → Verified.

---

## Burnout guardrails

- Max 40 h planned work; scope drops before sleep drops
- One “cooldown” week per quarter — bugs/docs only
- Celebrate M0, M1 — milestones are morale fuel

Next: [Part 11 — End-to-end workshop](11-end-to-end-workshop.md)
