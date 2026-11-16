# Foundations of the C.H. Method

C.H. organizes human–AI software engineering around explicit decisions, bounded delegation, evidence, and versioned memory.

## Values

The method prioritizes:

1. verifiable intent over lengthy or sophisticated prompts;
2. reproducible evidence over confident responses;
3. small, reversible slices over large autonomous deliveries;
4. explicit project memory over assumed conversational context;
5. human accountability over convenient autonomy;
6. fit-for-purpose orchestration over loyalty to a model or tool.

## Twelve principles

1. Every delivery has an identifiable accountable human, even if agents perform all implementation.
2. Work starts by understanding expected value, not by choosing a tool or writing a prompt.
3. Before acting, agents must consult the current source of truth: code, tests, contracts, decisions, and repository instructions.
4. Architectural, contractual, economic, or security changes require an explicit decision before implementation.
5. Each delegation specifies purpose, authorized scope, constraints, acceptance criteria, and a clear stop condition.
6. Execution occurs in an isolated environment and produces reversible changes, preferably in its own branch or worktree.
7. A claim of success never replaces evidence: diffs, tests, static analysis, working demonstrations, and known limitations.
8. Review depth and autonomy must vary with risk, impact, and reversibility.
9. Parallelism must be limited by the capacity to verify and integrate, not by the number of available agents.
10. Models, tools, and providers should be chosen for fitness to the task, considering capability, cost, privacy, and risk.
11. Relevant decisions, corrections, and lessons must return to the repository to reduce dependence on conversational memory.
12. The team must continually reduce technical debt, pattern drift, and entropy created by increased speed.

## Status

C.H. is an experimental proposal. Its principles should remain applicable, measurable, open to criticism, and capable of evolving.
