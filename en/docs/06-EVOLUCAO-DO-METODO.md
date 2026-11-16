# Evolution of the C.H. Method

This document distinguishes the **frozen historical record** from evolving practices.

## Preservation rule

Version 0.1, consolidated on August 27, 2026, must not be rewritten to look more mature than it was. New practices are recorded as evolutions, hypotheses, or later versions.

## Timeline

### August 2026 — practical origin

During development of Maestro Router, a human–AI workflow began to stabilize organically: human decision, small scope, bounded agent execution, evidence, review, and authorization before integration.

### August 27, 2026 — Experimental White Paper v0.1

The experience was formalized as the **C.H. Agile Method**.

It introduced:

- the dual meaning ChatGPT–Hallan / Hybrid Collaboration;
- six values;
- twelve principles;
- W Slices;
- the CHAVE cycle;
- roles and responsibilities;
- autonomy levels CH-0 through CH-3;
- Evidence Packages;
- integration gates;
- metrics and validation hypotheses.

Version 0.1 remains available in the [historical white paper](../whitepaper/WHITE-PAPER-v0.1.md).

### September 2026 — continued application to Maestro Router

The method continued to be exercised through real W Slices. Practice reinforced the separation between:

- product decisions;
- architecture decisions;
- execution;
- verification;
- integration authorization.

The need for separation between executor and reviewer, exact baselines before each W Slice, and gates against merging a different HEAD from the one reviewed also became clearer.

### September 2026 — the Economic C.H. hypothesis

Intensive use of agents exposed another bottleneck: **the cost of reasoning, context, and redundant review may grow faster than W Slice value**.

This observation led to a still-unvalidated operational evolution provisionally called **Economic C.H.**

It does not replace the v0.1 principles. It seeks to cut redundancy without removing safeguards:

1. match model capability to task difficulty;
2. escalate capability only when evidence justifies it;
3. avoid pasting large logs into the orchestrator's context;
4. inspect diffs progressively and selectively;
5. separate implementation review, architecture review, and independent gates;
6. measure savings per accepted W Slice, not by raw call counts;
7. start a fresh session when accumulated context ceases to be useful.

### Current status

**Economic C.H. is not a published historical version of the method.** It is an operational hypothesis under experimentation, to be included in later versions only after sufficient use, observation, correction, and documentation.

## How an evolution becomes part of the method

A new practice must pass through CHAVE:

**Contextualize → Harmonize → Act → Verify → Evolve**

Before promoting an experiment to a principle or recommended practice, there must be application evidence, known limitations, and a reason for inclusion.

## Commitment

The goal is not to preserve C.H. exactly as it was born, but to preserve **the truth of its origin** and let it evolve traceably.
