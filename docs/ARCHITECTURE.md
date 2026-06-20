# 🏗️ NEXUS Architecture

> System design and prompt composition model.

---

## 🎯 Architectural Overview

NEXUS is a **prompt-orchestrated cognitive workflow** that runs entirely within an LLM session. No external software, no orchestration framework, no API integration required.

This is deliberate. Frameworks tie methodology to implementation. Portable prompts work in any LLM, today and tomorrow, regardless of model architecture or vendor.

The architecture consists of five layers:

```
┌──────────────────────────────────────────────────────────┐
│  LAYER 1: MASTER DIRECTIVE                                │
│  Cognitive contract. Loaded once per session.             │
└──────────────────────┬───────────────────────────────────┘
                       ▼
┌──────────────────────────────────────────────────────────┐
│  LAYER 2: PHASE PROMPTS (01-07)                           │
│  Sequenced workflow. Run in order.                        │
└──────────────────────┬───────────────────────────────────┘
                       ▼
┌──────────────────────────────────────────────────────────┐
│  LAYER 3: ARCHETYPES (9)                                  │
│  Invoked by Phase 2; can also be used standalone.         │
└──────────────────────┬───────────────────────────────────┘
                       ▼
┌──────────────────────────────────────────────────────────┐
│  LAYER 4: DOMAIN PACKS (optional)                         │
│  Tunes archetypes and confidence for specific domains.    │
└──────────────────────┬───────────────────────────────────┘
                       ▼
┌──────────────────────────────────────────────────────────┐
│  LAYER 5: POLYMATH LAYER (optional)                       │
│  12 lenses + ~50 mental models + analogical engine.       │
└──────────────────────────────────────────────────────────┘
```

---

## 🧬 Composition Model

The layers compose through **inheritance and invocation**:

- **Inheritance:** Every prompt inherits the Master Directive's principles. Subsequent layers do not restate these — they operate within the established cognitive contract.

- **Invocation:** Phase 2 invokes all 9 archetypes. A domain pack invocation modifies how each archetype is interpreted. The Polymath layer adds 12 lenses + 50 mental models as additional invokable cognitive tools.

The user's job is sequencing. Master Directive + Phases 1-7 is the **mandatory minimum**. Domain packs and Polymath Mode are opt-in extensions.

---

## 📐 Inheritance Diagram

```
                  ┌──────────────────────────────┐
                  │   MASTER DIRECTIVE           │
                  └──────────────┬───────────────┘
                                 │
                  ┌──────────────┴───────────────┐
                  ▼                              ▼
       ┌─────────────────────┐        ┌─────────────────────┐
       │  PHASE PROMPTS      │        │  DOMAIN PACK        │
       │  01_grounding       │        │  (finance / EA /    │
       │  02_archetypes      │◄───────│   healthcare /      │
       │  03_dialectic       │        │   ai_strategy /     │
       │  04_evidence        │        │   investment)       │
       │  05_blindspots      │        └─────────────────────┘
       │  06_temporal        │
       │  07_decision_brief  │
       └──────────┬──────────┘
                  │
        ┌─────────┴──────────┐
        ▼                    ▼
┌──────────────┐    ┌──────────────────────┐
│ ARCHETYPES   │    │  POLYMATH LAYER      │
│ 01-09        │    │  (optional)          │
└──────────────┘    └──────────────────────┘
```

---

## 🔄 Stateless vs Stateful Considerations

NEXUS is currently **stateless across sessions** — each new session starts fresh. This is by design. Stateful systems require infrastructure that would undermine the portability principle.

**For users who want stateful behavior:** Maintain a manual log of NEXUS sessions in your preferred note system. The most valuable cross-session pattern to track is which archetypes consistently produce the strongest insights in your domain.

A future version may add an optional Python layer for vector-DB-backed session memory. It is not on the current roadmap.

---

## 🌐 Tool Independence

NEXUS is designed to run in any LLM:

- **Claude (Anthropic)** — strongest on Adversarial Dialectic Engine
- **GPT-4 / GPT-5 (OpenAI)** — strong on Polymath Mode analogical reasoning
- **Copilot (Microsoft)** — works with shorter response patterns
- **Gemini (Google)** — works
- **Local models (Llama 3+ class)** — works, with degraded quality on adversarial debates

There is no LLM-specific dependency. If the model can follow a multi-step prompt, NEXUS works.

---

## 🔧 Polymath Layer Integration

The Polymath layer slots between Phase 3 and Phase 7:

```
Phase 1 → Phase 2 → Phase 3
                       │
                       ▼
         ┌──────────────────────────────┐
         │  POLYMATH MODE (optional)    │
         │  1. 12 Domain Lenses         │
         │  2. Mental Models Library    │
         │  3. Analogical Reasoning Eng │
         └──────────────┬───────────────┘
                       ▼
Phase 4 → Phase 5 → Phase 6 → Phase 7
```

Phase 4 then grades both standard NEXUS insights AND Polymath insights on the same 4-factor confidence matrix. Polymath insights get no special treatment.

---

## ⚙️ Extensibility

NEXUS is designed for extension in four directions:

1. **New domain packs** — specialized tunings for regulated industries or technical fields
2. **New worked examples** — the strongest form of methodology validation
3. **Mental model additions** — the polymath library is bounded but not closed
4. **Translations** — porting prompts to other languages, preserving brutal-accuracy tone

What is **not** extensible: the Master Directive itself. Politically motivated edits to soften it are rejected by design.

---

## 🛡️ Failure Modes & Mitigations

| Failure Mode | Mitigation |
|---|---|
| User forgot to paste Master Directive | Output feels generic — restart session |
| Domain pack activated without Master Directive | Output lacks confidence calibration — restart |
| Polymath Mode invoked for routine problem | Output is decorative and unactionable — skip Polymath |
| All 9 archetypes converge too easily | Force re-running Phase 2 with explicit differentiation |
| Confidence grading inflated (everything HIGH) | Re-run Phase 4 with "minimum across 4 factors" reminder |
| Analogical analogs are surface-only | Re-run with Step 7 (stress test) forced |

These failure modes are documented because they are real. Honest documentation is itself part of the methodology.
