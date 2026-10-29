# Part 99 — FAQ, Anti-Patterns & Cheat Sheet

---

## FAQ

**Q: Epic vs feature vs story — where do I cut?**  
A: Epic = capability theme. Feature = user recognizes it in release notes. Story = one AC set, one sprint slice. If > 5 points, split story.

**Q: How many REQs for MVP?**  
A: Often 25–60 FR + 10–15 NFR for a small product; weekend prototype 5–10 FR total.

**Q: Do I need every document in Part 14?**  
A: Minimum: charter, requirements register, RTM, ADRs for big forks. Add PRD lite if collaborators join.

**Q: RTM is stale — what now?**  
A: Stop new features 2 h; update RTM from main branch; add PR rule. Stale RTM = technical debt.

**Q: I only build for myself.**  
A: Still use REQ IDs and AC — “future you” is the stakeholder who forgot why.

**Q: Agile says no big design upfront — contradicts SRS?**  
A: Agile rejects **frozen wrong big design**. Living SRS in git is agile-compatible.

**Q: How trace bugs?**  
A: Bug → REQ-ID regression → fix PR → TEST-* prevents repeat.

**Q: Can one story map to many REQs?**  
A: Yes. RTM is many-to-many.

**Q: When write use cases?**  
A: Payment, auth, multi-actor, compliance flows.

**Q: Waterfall client wants Gantt?**  
A: Export milestone roadmap from Part 25; keep internal agile; RTM satisfies audit.

---

## Anti-patterns encyclopedia

| Anti-pattern | Symptom | Fix |
|--------------|---------|-----|
| **Screen-driven breakdown** | Backlog = pages | Journey → capabilities |
| **Zombie epic** | EP-01 open forever | Close; split done features |
| **REQ in chat only** | No ID in code | Register + label issues |
| **Testing theater** | 100% coverage, wrong behavior | AC-linked TEST-* |
| **Infinite MVP** | Must never shrinks | Charter non-goals |
| **Horizontal sprint** | “All API week” | Walking skeleton |
| **Duplicate truth** | Notion + sheet + git differ | Git wins |
| **13-point story** | Never finishes | Split vertically |
| **Skip NFRs** | Launch day fire | Part 21 catalog |
| **No waiver trail** | Silent scope cut | RTM waiver column |

---

## One-page cheat sheet

### Breakdown chain
Who → JTBD → Journey step → REQ → Epic → Feature → Story + AC → Task (≤1d)

### IDs
`REQ-FR-*` `US-*` `TEST-*` `EP-*` `ADR-*` `R-*`

### Ready (DoR)
REQ linked · AC written · deps known · test approach

### Done (DoD)
AC met · tests · RTM · docs if user-visible

### Weekly solo
Plan 3 outcomes · WIP 2 · mid-week cut · Fri demo + retro + RTM

### Prioritize
Must ≤60% effort · walking skeleton first · learning spikes early

### Trace
Every Must REQ → story → test → release Verified

---

## Maintenance of this knowledge

When you learn a gap in the field:

1. Add row to [STUDY-PATH.md](../STUDY-PATH.md) concept matrix  
2. Add glossary entry in [Part 0](00-glossary-and-map.md)  
3. PR to your fork — treat the guide as living REQ set  

Return to [README](../README.md).
