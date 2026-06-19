# ⚔️ Phase 3 — Adversarial Dialectic Engine

> **Purpose:** Force the 9 archetypes to argue with each other in structured debates. This is the strongest single innovation in NEXUS vs STORM.

---

## 📋 Prerequisites

- ✅ Master Directive loaded
- ✅ Phase 1 (Context Grounding) complete
- ✅ Phase 2 (9 Archetypes) complete

---

## 🎯 Why This Phase Matters

STORM identifies contradictions in a separate post-hoc step — perspectives don't actually argue.

NEXUS forces **structured debate** with explicit format: Opening → Counter → Rebuttal → Common Ground → Unresolved Tension.

This produces:
- Sharper diagnostic clarity
- Better-calibrated confidence
- Clearer escalation flags for issues requiring human judgment

---

## 📜 The Prompt (Copy Below)

```
[NEXUS Phase 3 — Adversarial Dialectic Engine]

Based on the 9 archetypes from Phase 2, run 5 structured debates.
Apply the Master Directive — no hedging, lead with the strongest counter,
explicit confidence levels.

Each debate uses this exact format:

  • OPENING CLAIM (Archetype A) — 2-3 sentences, sharpest version
  • STRONGEST COUNTER (Archetype B) — most damaging counter-argument
  • REBUTTAL (Archetype A) — does the opening claim survive?
  • COMMON GROUND — what do they actually agree on (if anything)?
  • UNRESOLVED TENSION — what stays in conflict and why?

═══════════════════════════════════════════════════════════
DEBATE 1 — Theory vs Reality
  🛠️ PRACTITIONER vs 🎓 ACADEMIC
  Topic: Where does the academic consensus break down in practice?

DEBATE 2 — Incentives vs Ethics
  💰 ECONOMIST vs ⚖️ REGULATOR
  Topic: Where do market incentives conflict with systemic safety?

DEBATE 3 — Past patterns vs Future scenarios
  📜 HISTORIAN vs 🔮 FUTURIST
  Topic: Is this situation a repeat of a known pattern, or genuinely novel?

DEBATE 4 — Public skepticism vs Insider knowledge
  🤔 SKEPTIC vs 🕵️ INSIDER
  Topic: Is the public critique aimed at the real problem, or a decoy?

DEBATE 5 — The Contrarian vs Everyone
  🔥 CONTRARIAN vs ALL OTHER 8 ARCHETYPES
  Topic: What if the entire framing of this problem is backwards?
═══════════════════════════════════════════════════════════

After all 5 debates, output:

A. CONVERGENCE
   What did most or all archetypes agree on, even after debate?
   (These are the highest-confidence findings.)

B. PERSISTENT DISAGREEMENT
   What remained unresolved after debate?
   For each: what evidence would settle it?

C. ESCALATION FLAGS
   Which questions are too important and too uncertain to resolve via
   AI debate alone? These require human expert intervention.
   Be specific about WHO should be consulted.

D. CONFIDENCE RECALIBRATION
   For each finding from Phase 2, mark whether the debate raised or lowered
   confidence (HIGH/MODERATE/LOW/UNKNOWN), and why.
```

---

## 📤 Expected Output

5 structured debates, each with the 5-element format. Followed by A/B/C/D summary sections with explicit confidence recalibration.

---

## 💡 Tips

- **The Contrarian debate (Debate 5) is often the most valuable.** It frequently exposes structural assumptions that the other 8 archetypes share without noticing.
- **Persistent disagreements are signals, not failures.** Unresolved tensions point to genuinely open questions worth pursuing.
- **Escalation flags are golden.** If the AI flags something as requiring human expert input, take it seriously.

---

## ⏭️ Next Step

`04_evidence_weighting.md` — Grade every surviving claim on a 4-factor confidence matrix.
