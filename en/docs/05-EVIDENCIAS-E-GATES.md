# Evidence and Gates

In C.H., trust alone is not an acceptance criterion. Deliveries must produce evidence proportional to risk.

## Minimum Evidence Package

| Block | Expected evidence |
|---|---|
| **Identity** | W Slice, executor, model, environment, branch, and baseline. |
| **Changes** | Diff summary and changed files. |
| **Checks** | Tests, static analysis, build, and functional demo when applicable. |
| **Scope** | Confirmation of scope compliance; deviations must be declared. |
| **Risk and security** | Secrets, data, network, dependencies, permissions, and destructive operations. |
| **Limitations** | Assumptions, untested cases, questions, and deferred decisions. |
| **Economics** | Time, known usage/cost, and reason for choosing the executor, when measurable. |
| **Final state** | Commit, Draft PR, working tree state, and rollback strategy. |

## Gates

Gate depth follows risk, impact, and reversibility. A typical flow separates:

**execution → evidence → independent review → human acceptance → integration**

A Draft PR is a request to integrate, not proof of completion. Passing tests does not replace requirements, architecture, security, or scope review.

## Useful metrics

C.H. favors accepted value and supervision cost: accepted W Slice throughput, first-pass acceptance, correction loops, verification effort, escaped defects, scope drift, integration conflicts, and cost per accepted W Slice.
