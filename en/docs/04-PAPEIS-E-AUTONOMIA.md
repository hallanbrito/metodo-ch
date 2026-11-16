# Roles and Autonomy

C.H. defines **responsibilities**, not fixed job titles. People and agents may hold multiple roles, but human accountability must not be confused with agentic execution.

## Roles

| Responsibility | Function |
|---|---|
| **Human Owner** | Defines value, priority, acceptable risk, and final approval. Remains accountable for the product. |
| **Cognitive Orchestrator** | Turns intent into decisions and W Slices, selects agents, bounds scope, identifies conflicts, and coordinates reviews. |
| **Agentic Executor** | Executes the W Slice in the authorized environment, changes only permitted scope, and produces evidence. |
| **Evidence Guardian** | Checks criteria, challenges assumptions, and evaluates security and coherence with sufficient independence. |
| **Memory Maintainer** | Keeps instructions, maps, decisions, contracts, standards, and lessons in the versioned source of truth. |

## Autonomy levels

Autonomy is granted **per W Slice** and calibrated to risk.

| Level | Name | Permission |
|---|---|---|
| **CH-0** | Consult | Read, analyze, and explain only. No external changes. |
| **CH-1** | Propose | May prepare a plan, decision, prompt, or suggested diff without writing to the source of truth. |
| **CH-2** | Execute in isolation | May create a branch, modify authorized scope, test, commit, and open a Draft PR. Cannot integrate. |
| **CH-3** | Conditional integration | May integrate low-risk changes when predefined gates and policies pass, leaving an audit trail. |

Higher levels never override special policies for destructive operations, secrets, production, personal data, or external contracts.

## Responsible parallelism

Having several agents does not make parallel work mandatory. Work-in-progress limits depend on review capacity and coupling between W Slices.
