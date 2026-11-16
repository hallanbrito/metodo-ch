# Essential documentation — only what you need

> **A new developer or AI agent should be able to continue the project without depending on an old chat.**

This C.H. Method operational guide does not require files for their own sake. **Reuse what works.** Code, tests, Git, Issues, and PRs provide verifiable sources; do not create a conflicting second version of project state.

## The minimum recipe

| Record | Purpose | When? |
|---|---|---|
| `README.md` | What it is, how to install, run, and test | Every shared repository |
| `docs/STATUS.md` **or** Issue/Project | What works, what is blocked, and what comes next | Long-running or multi-agent projects |
| `AGENTS.md` **or** equivalent instructions | How agents must work, test, and stop | Repeated AI-assisted work |
| Issue **or** [W Slice](../templates/FATIA-W.md) | One task, boundaries, and acceptance criteria | Before delegating changes |
| PR **or** [Evidence Package](../templates/PACOTE-DE-EVIDENCIAS.md) | Diff, tests, and review | Before accepting delivery |

**Only if needed:** `ARCHITECTURE.md` (non-obvious architecture), ADR/Issue (lasting decision), `SECURITY.md` (reporting policy), and changelog (releases). Simplicity never overrides necessary risk controls.

## `STATUS.md` in a few lines

~~~markdown
# Project state
- Updated: <date, owner, branch, commit>
- Works: <result + test or PR>
- In progress: <Issue + owner>
- Blocked: <problem + evidence>
- Current decision: <link>
- Next authorized task: <one W Slice + autonomy>
- Not verified: <limitation>
~~~

**Important:** STATUS is a **linked summary**, not a second Kanban board. Update it only when real state changes. If the Project/Issues are sufficient, skip this file.

## `AGENTS.md` in a few lines

~~~markdown
# Instructions for AI agents
- First: read README, project state, delegated Issue; check HEAD.
- Scope: change only what is authorized; escalate extra decisions.
- Commands: <installation, tests, build actually verified>
- Limits: no merge, deploy, spend, or destruction without permission.
- Delivery: diff, tests actually run, limitations, PR.
- Stop: <condition agreed with the accountable human>
~~~

Not every AI tool reads `AGENTS.md` automatically. Supply instructions through the supported channel. **Never commit secrets.**

## Daily cycle — no extra ceremony

1. **Start:** confirm README, state source, Issue, and commit.
2. **Act:** one small W Slice with clear boundaries and acceptance.
3. **Verify:** show what changed, what ran, and what failed.
4. **Finish:** record the decision, evidence, and next action **where these already belong**.

**Antipatterns:** duplicating logs, creating conflicting status files, reporting tests that never ran, or updating documents without meaningful changes.

**Final principle: the best documentation is the smallest amount that lets the team continue safely.**

*Evolving operational practice; the historical manifesto and white paper v0.1 are preserved.*
