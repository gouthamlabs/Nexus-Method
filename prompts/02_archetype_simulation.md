# 🎯 Phase 1 — Context Grounding

> **Purpose:** Establish what is being researched, for whom, on what time horizon, and what "good understanding" looks like — *before* any analysis begins.

---

## 📋 Prerequisites

- ✅ Master Directive loaded (`00_master_directive.md`)
- ✅ Topic or decision question clearly framed

---

## 📜 The Prompt (Copy Below)

```
[NEXUS Phase 1 — Context Grounding]

Topic: [REPLACE WITH YOUR TOPIC OR DECISION QUESTION]

Before any analysis, establish the following grounding card.
Apply the Master Directive: no hallucination, explicit confidence levels, no validation language, lead with counterargument if my framing is wrong.

1. DOMAIN CLASSIFICATION
   What primary domain(s) does this belong to?
   Are there hidden cross-domain dependencies I have not stated?
   If my framing of the domain is wrong, say so immediately.

2. DECISION HORIZON
   Is this strategic (5+ years), tactical (1-3 years), or operational (now/next quarter)?
   What is the cost of delaying the decision?
   What is the cost of deciding wrong?

3. STAKEHOLDER MAP
   Who is affected by this decision or topic?
   Who benefits if the consensus view is right?
   Who loses if the consensus view is wrong?
   Whose voice is structurally missing from current discourse?

4. UNCERTAINTY PROFILE
   - Known knowns: What is reasonably well-established?
   - Known unknowns: What questions remain open?
   - Unknown unknowns: What entire categories might we be missing?
   Mark each item with explicit confidence (HIGH / MODERATE / LOW / UNKNOWN).

5. SUCCESS DEFINITION
   What does "good understanding" of this topic actually look like?
   What would make the eventual decision/output verifiably correct or wrong?
   How would we know in 6 months whether we got this right?

6. REFRAMING CHECK
   Is the question itself well-posed?
   Is there a sharper version of this question that would produce better analysis?
   If yes, propose it explicitly — do not silently substitute.

Output as a structured grounding card with one section per item.
Be specific. No hedging. No disclaimers.
```

---

## 📤 Expected Output

A structured card with all six sections filled, explicit confidence levels on uncertainty items, and a sharper reframing of the question if the original is sub-optimal.

---

## 💡 Tips

- **Be specific in your topic.** "AI in healthcare" is a weak topic. "Why do clinical AI deployments succeed in pilots and fail at scale-up?" is a strong topic.
- **Welcome reframing.** If the AI proposes a sharper question, consider adopting it before proceeding to Phase 2.
- **Reread the grounding card before Phase 2.** It's the foundation everything else rests on.

---

## ⏭️ Next Step

`02_archetype_simulation.md` — Run the 9 expert archetypes against the grounded question.
