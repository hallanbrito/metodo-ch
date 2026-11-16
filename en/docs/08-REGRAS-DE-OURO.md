# 10 Golden Rules — Humans + AI

> **Build with AI. Decide as a human. Accept with evidence.**

This is a practical guide to the [C.H. Method](../README.md). It does not depend on any vendor, agent, or model. For details, see [Foundations](01-FUNDAMENTOS.md), [W Slices](03-FATIAS-W.md), and [Autonomy](04-PAPEIS-E-AUTONOMIA.md). The English links refer to the bilingual documentation prepared in PR #4.

## The recipe

1. **Chats are not the source of truth.** Read versioned code, tests, Issues, PRs, and decisions. Use `STATUS.md` when it helps the team resume work.
2. **Inspect before proposing.** Find out what already works and what has already been tested. Do not invent prerequisites.
3. **Keep one W Slice small.** One outcome, boundaries, and acceptance criteria. Size is defined by reviewability, not a universal 20-line or one-file rule.
4. **Use KISS and YAGNI.** No new service, framework, or dependency without a demonstrated need. Necessary security is not overengineering.
5. **Assign roles, not brands.** An accountable human decides; an orchestrator organizes; an executor implements; a reviewer verifies. Tools are replaceable.
6. **Ask for proof, not promises.** Diffs, tests actually run, observed behavior, and limitations. Say when checks were not run.
7. **Stop circular bureaucracy.** A step, gate, or script must reduce a real risk or repeated work.
8. **Delegate within boundaries.** Define allowable changes, access, cost, autonomy, and stop conditions. Production and destructive operations need extra control.
9. **Learn once.** Record decisions, failures, and next steps in the repository rather than rediscovering them every chat.
10. **Measure accepted value.** Quality, rework, and review effort matter more than prompts, lines of code, or agent count.

## Emergency reset

> **STOP — KISS.** Consult the versioned project state. Do not repeat tests without a reason or create stages without real risks. Show one minimal W Slice: outcome, boundaries, acceptance check, and next action. Ask a human when authorization is missing.

## Minimal prompt

~~~text
Project and baseline: <repo, branch, commit>
Goal: <one observable result>
Source of truth: <code, Issue, decisions, tests>
Allowed changes: <scope>
Forbidden changes: <exclusions>
Acceptance: <how to prove it>
Autonomy: <CH-0 through CH-3>
Stop: <when to hand back to the human>
~~~

**Final rule:** the method must reduce the developer's mental load, not add work to appear professional.

*Evolving operational practice. Historical manifesto v0.1 remains unchanged.*
