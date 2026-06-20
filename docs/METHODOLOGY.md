# 📚 NEXUS Methodology

> The full theoretical foundation of the 7 phases, 9 archetypes, and the inheritance model.

---

## 🎯 Overview

NEXUS is a structured prompting methodology for AI-assisted executive decision-making. It compresses the cognitive workflow of a senior analyst — context grounding, multi-perspective synthesis, adversarial stress-testing, confidence calibration, blind-spot detection, temporal layering, and decision compilation — into seven sequenced prompts.

It is not a software framework. It is a portable thinking pattern that runs in any LLM. The intellectual property is in the prompt design, archetype definitions, and phase sequence — not in code.

---

## 🧭 Design Principles

### 1. Calibrated Confidence Over False Certainty
Every substantive claim is graded HIGH / MODERATE / LOW / UNKNOWN. Non-negotiable because it makes the analysis debuggable.

### 2. Augment, Not Replace
NEXUS does not replace domain expertise. It amplifies it. A NEXUS session run by a domain expert produces significantly better output than one run by a novice — the method exposes weak claims an expert can challenge.

### 3. Empirical Validation Over Elegance
The method has been triangulated across three substantial worked examples in radically different domains. Where empirical findings contradict the elegant design, the empirical finding wins.

### 4. Explainability First
Every output traces back to specific archetypes and evidence. There are no black-box conclusions. A reader can ask "why does the analysis claim X?" and find the answer.

### 5. Dialectical Reasoning
The Adversarial Dialectic Engine (Phase 3) is the strongest single innovation. Forcing structured debate between archetypes produces sharper diagnostics than parallel perspectives.

### 6. Automation-First
Fully automated within the LLM session. No manual steps between prompts.

---

## 🎬 The 7 Phases in Detail

### Phase 1: Context Grounding
**Cognitive purpose:** Force the analyst to define the question before answering it. Most analytical failures occur in the framing, not the analysis. Phase 1 establishes domain, decision horizon, stakeholder map, uncertainty profile, success definition, and a reframing check.

### Phase 2: 9-Archetype Expert Simulation
**Cognitive purpose:** Force the topic through 9 sharply distinct expert lenses. Each archetype is calibrated to see something the others miss. The Insider and Contrarian archetypes routinely produce insights absent from mainstream analysis.

### Phase 3: Adversarial Dialectic Engine
**Cognitive purpose:** Force the 9 archetypes to argue with each other rather than just generate parallel statements. Five structured debates with explicit format: Opening → Counter → Rebuttal → Common Ground → Unresolved Tension.

**This is the strongest single differentiator vs Stanford STORM**, which identifies contradictions in a post-hoc step without forcing actual debate.

### Phase 4: Evidence Weighting & Confidence Grading
**Cognitive purpose:** Make uncertainty visible and traceable. Every claim is graded on a 4-factor matrix (Evidence Strength × Source Quality × Recency × Domain Expertise Alignment). Final confidence is the **minimum** across factors — intentionally conservative.

### Phase 5: Blind Spot & Counterfactual Analysis
**Cognitive purpose:** Attack the analysis before reality does. Pre-mortem, counterfactual, blind spot detection, bias audit, missing 10th archetype. Most AI research stops at Phase 2 or 3 — the moment of maximum risk.

### Phase 6: Temporal Synthesis
**Cognitive purpose:** Layer the analysis across past patterns (Historian leads), present reality (Practitioner leads), and future scenarios (Futurist leads with Best/Base/Worst cases and leading indicators).

### Phase 7: Decision Brief & Action Plan
**Cognitive purpose:** Compile everything into a decision-ready document. One-paragraph CEO summary, 5 key findings ranked by confidence, hidden connection, actionable insight, frontier question, confidence matrix, action plan with reversibility analysis, brutal honest verdict.

---

## 🎭 The 9 Archetypes — Why These 9

Selected through iterative experimentation. The principles:

1. **Each must see something the others would miss.** Overlapping archetypes were merged or removed.
2. **The set must include perspectives often absent from mainstream analysis.** This is why Insider, Contrarian, and Regulator are explicitly included.
3. **The set must be small enough to run in a single session.** Beyond 9, output quality degrades from cognitive overload.
4. **The set must work across domains.** Specialized archetypes are deferred to domain packs.

Full definitions in `../prompts/archetypes/`, each with explicit structural blind spots.

---

## 🧬 Inheritance Model

```
Master Directive (cognitive contract)
        │
        ▼
Phase Prompts (01-07)
        │
        ▼
Archetypes (01-09) ◄────┐
        │               │
        ▼               │
Domain Packs (5) ───────┘
        │
        ▼
Polymath Layer (optional)
```

Users only paste the Master Directive once per session. Every subsequent prompt operates under its constraints automatically.

---

## 🤝 Lineage from Stanford STORM

NEXUS builds directly on Stanford OVAL Lab's STORM method (Shao et al., NAACL 2024). STORM proved that multi-perspective AI research is more organized and comprehensive than single-shot prompting.

NEXUS extends that insight from *article generation* into *executive decision-making*. Full comparison in `COMPARISON.md`.

The structural innovations in NEXUS — Adversarial Dialectic Engine, explicit 4-tier confidence grading, temporal synthesis, domain packs, optional Polymath Mode — are genuine additions. The foundational insight (multi-perspective questioning) is STORM's.

---

## ⚠️ Known Limitations

1. **Cross-domain hallucination risk in Polymath Mode.** Polymath is opt-in with explicit mitigations.

2. **Domain expertise is still required.** A novice running NEXUS will produce plausible-sounding output an expert can see is wrong.

3. **Some lenses underperform consistently.** Triangulation showed Linguistics and Art & Design (Tier 3) frequently produce clever framing but weak operational prescriptions.

4. **Fragile to "forgotten Master Directive" sessions.** If user skips the directive paste, output quality degrades sharply.

5. **Political feasibility is not modeled.** NEXUS can produce optimal recommendations that are politically impossible to implement.
