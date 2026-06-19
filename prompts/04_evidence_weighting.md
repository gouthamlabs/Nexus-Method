# 📊 Phase 4 — Evidence Weighting & Confidence Grading

> **Purpose:** Apply a rigorous 4-factor confidence matrix to every claim that survived the adversarial debate. Make uncertainty *visible and traceable*.

---

## 📋 Prerequisites

- ✅ Master Directive loaded
- ✅ Phases 1-3 complete (Grounding → Archetypes → Debate)

---

## 🎯 The 4-Factor Confidence Matrix

Every claim is graded on four orthogonal dimensions:

| Factor | What It Measures |
|---|---|
| **Evidence Strength** | Quality, replicability, and quantity of supporting evidence |
| **Source Quality** | Credibility of the sources (peer-review, primary data, expert consensus) |
| **Recency** | How current the evidence is — for fast-moving domains this matters enormously |
| **Domain Expertise Alignment** | Whether the evidence comes from people who actually work in this domain |

Final confidence label is the **minimum** across the four factors — a single weak dimension drops overall confidence.

---

## 📜 The Prompt (Copy Below)

```
[NEXUS Phase 4 — Evidence Weighting & Confidence Grading]

For every substantive claim that survived Phase 3 debates, grade it on a
4-factor confidence matrix. Apply the Master Directive — no hedging,
no inflated confidence to make me feel better.

For each claim, output:

  CLAIM: [restate the claim in 1 sentence]

  4-FACTOR MATRIX:
    1. Evidence Strength:           HIGH / MODERATE / LOW / UNKNOWN
       Justification: [1-2 sentences]
    2. Source Quality:              HIGH / MODERATE / LOW / UNKNOWN
       Justification: [1-2 sentences]
    3. Recency:                     HIGH / MODERATE / LOW / UNKNOWN
       Justification: [1-2 sentences]
    4. Domain Expertise Alignment:  HIGH / MODERATE / LOW / UNKNOWN
       Justification: [1-2 sentences]

  OVERALL CONFIDENCE: [minimum of the four — HIGH/MODERATE/LOW/UNKNOWN]

  WHAT WOULD CHANGE THIS GRADE:
    [Specific evidence or developments that would raise or lower confidence]

After grading all claims, produce a CONFIDENCE LEDGER:

  HIGH confidence claims:
    - [list with brief restatement]
  MODERATE confidence claims:
    - [list with brief restatement]
  LOW confidence claims:
    - [list with brief restatement]
  UNKNOWN (insufficient information to grade):
    - [list with brief restatement]

Then identify:
  - Which 3 claims have the MOST evidence?
  - Which 3 claims are the most LOAD-BEARING but lowest confidence?
    (These are the highest-risk claims in the analysis.)
  - Where is the analysis OVER-CONFIDENT relative to actual evidence?
```

---

## 📤 Expected Output

A claim-by-claim 4-factor grade, followed by a confidence ledger sorted by tier, followed by three diagnostic findings (most-supported, highest-risk, over-confident).

---

## 💡 Tips

- **Pay special attention to load-bearing low-confidence claims.** These are the analysis's structural weak points — they support major conclusions but rest on shaky evidence.
- **Over-confidence flagging is critical.** If the AI flags itself as over-confident anywhere, that's an honest signal worth tracking.
- **HIGH confidence does not mean "true."** It means well-supported. Black swans live in HIGH-confidence claims that turned out to be wrong.

---

## ⏭️ Next Step

`05_blindspot_analysis.md` — Run a structured pre-mortem and counterfactual analysis.
