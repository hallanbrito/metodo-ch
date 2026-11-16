**EXPERIMENTAL WHITE PAPER | VERSION 0.1**

# The C.H. Agile Method

Human–AI software engineering guided by decisions,  
bounded delegation, and evidence

> *A method to accelerate software development with AI agents without outsourcing judgment, accountability, or quality.*

**Created by Hallan de Sousa Brito and ChatGPT (OpenAI)**

Human conception and responsibility: Hallan de Sousa Brito

Conceptual collaboration and assisted writing: ChatGPT

**Born from the experience of building Maestro Router**

Teresina, Brazil | August 27, 2026

> **Translation notice:** This is an English translation of the [historical Portuguese White Paper v0.1](../../whitepaper/WHITE-PAPER-v0.1.md). The Portuguese document is the original historical record. The translation does not introduce a new method version.

## Abstract

The C.H. Agile Method is an experimental proposal to organize software development by hybrid teams of people and artificial intelligence agents. Its acronym records the original collaboration — ChatGPT–Hallan — and also expresses its general principle: Hybrid Collaboration (*Colaboração Híbrida*). The method emerged during the incremental development of Maestro Router in 2026, when code generation stopped being the main bottleneck and work shifted toward defining decisions, limiting delegated scope, verifying results, and maintaining product coherence.

The proposal does not replace the Agile Manifesto, Scrum, Kanban, or Extreme Programming. It inherits incremental delivery, frequent feedback, simplicity, technical quality, and adaptation from these traditions. Its contribution is to make explicit problems now central to agentic software engineering: who is accountable for decisions, how much autonomy AI receives, how context is preserved, which evidence permits delivery acceptance, and how much parallel work human verification capacity can support.

C.H. organizes work into verifiable W Slices and uses the CHAVE cycle: Contextualize, Harmonize, Act, Verify, and Evolve. Final responsibility remains human. Agents can plan, implement, test, document, and review, but a result is never accepted merely because it was generated confidently or quickly. The method is presented as an operational hypothesis open to experimentation, measurement, and public revision.

> **Central thesis.** In AI-assisted engineering, sustainable productivity is not the amount of code generated. It is the amount of value accepted with evidence, understanding, and accountability.

**Keywords:** agile methods; agentic software engineering; human–AI collaboration; coding agents; governance; verification; incremental development.

## 1. Introduction: Code Became Faster; Accountability Did Not

The Agile Manifesto of 2001 responded to heavy processes and the distance between planning and delivery. Its values remain relevant: people, useful software, collaboration, and adaptation still matter [1]. Scrum consolidated empirical cycles of transparency, inspection, and adaptation [2], while XP practices emphasized small deliveries, testing, integration, and continuous improvement. C.H. does not arise from rejecting this history. It arises from recognizing a new participant in software production: an AI agent able to read repositories, edit multiple files, run tools, create tests, and propose pull requests.

In 2026, such an agent is more than an autocomplete tool. It can receive a task, explore code, change an implementation, and return a set of changes for review. OpenAI engineering reports describe workflows in which agents operate through prompts, open pull requests, respond to reviews, and work on long-running tasks; the same reporting identifies human quality-assurance capacity as a new bottleneck [5]. The change is organizational: when writing code becomes cheap, producing *too much* code also becomes cheap.

Adoption does not eliminate risk. In the 2025 Stack Overflow survey, 84% of respondents were using or planning to use AI in development, but 46% said they distrusted tool accuracy, compared with 33% who trusted it. Among frustrations, 66% mentioned nearly correct solutions and 45% said debugging AI-generated code took more time [4]. The 2025 DORA research summarizes AI as an amplifier of strengths and weaknesses already present in an organization [3].

The problem motivating C.H. can therefore be stated simply: existing methods guide iterative delivery by human teams, but usually do not specify how to delegate work to probabilistic agents, limit their autonomy, preserve memory across sessions, compare models, prove results, and control generation speed that may exceed review capacity.

## 2. Origins and Positioning

### 2.1 A Name with Two Meanings

C.H. originally stands for ChatGPT–Hallan, recording the collaboration that gave rise to the method: Hallan de Sousa Brito as Product Owner, practitioner, and accountable human; ChatGPT as an architecture, analysis, and writing collaborator; and coding agents, especially Codex, as bounded executors. To make the proposal applicable to other teams, the acronym also stands for Hybrid Collaboration (*Colaboração Híbrida*): people define purpose and assume responsibility, while agents expand analysis and execution capacity.

This dual meaning preserves the origin without turning the method into a vendor-dependent recipe. C.H. is explicitly model-neutral. Teams may use ChatGPT, Codex, Claude, Gemini, local models, or future tools, provided each executor works within verifiable limits.

### 2.2 What C.H. Does Not Claim

C.H. does not claim to be the first attempt to integrate agility and AI. AgileGen, published in 2025, explored generative software development based on human–AI collaboration and testable requirements, focusing on consistency between requirements and code [7]. By 2026, research also began addressing agentic software engineering as a field of its own and studying concrete forms of human oversight [8].

C.H.'s specific contribution is operational: bringing decisions, bounded delegation, project memory, isolated execution, evidence, cost, autonomy, and review capacity together in one lightweight flow. Its basic unit is not the user story, Sprint, or prompt. It is the W Slice: a small, justifiable, reversible, and verifiable change.

> **Proposal status.** Version 0.1 is a conceptual white paper based on an initial case study. The method still needs application by other teams and experimental comparison with alternative workflows.

## 3. The Shift in Software Engineering's Bottleneck

Traditional engineering treated implementation as a scarce resource: people needed to translate requirements into code line by line. Generative tools and agents reduce part of that cost but create an asymmetry. An agent can produce more changes than a person can safely understand, test, and integrate.

Anthropic's internal studies reported more work output, expanded technical roles, and faster learning, alongside concerns about losing deep skills, difficulty supervising, and reduced collaboration among colleagues [6]. Research with experienced developers identified four kinds of oversight over agents: prior control, joint planning, monitoring during execution, and retrospective review [8]. The actual Maestro Router workflow exhibited similar needs before those categories received formal names.

C.H. starts from three shifts:

- From writing every line to defining intent, architecture, and acceptance criteria.
- From tracking human effort to controlling agent autonomy, context, cost, and risk.
- From trusting the implementer's ability to requiring reproducible evidence of what was delivered.

> **Verification capacity law.** A human–AI team's sustainable flow is limited by the smallest of execution, verification, and integration capacity. Adding agents does not increase throughput when review or integration is already the bottleneck.

## 4. The Six Values of C.H.

The items on the right still have value; C.H. establishes which ones take priority in a conflict.

| # | We value | Over |
|---|---|---|
| 1 | Verifiable intent | long or sophisticated prompts |
| 2 | Reproducible evidence | confident responses |
| 3 | Small, reversible slices | large autonomous deliveries |
| 4 | Explicit project memory | assumed conversational context |
| 5 | Human accountability | convenient autonomy |
| 6 | Fit-for-purpose orchestration | loyalty to a model or tool |

## 5. The Twelve Principles

1. Every delivery has an identifiable accountable human, including when agents perform all implementation.
2. Work begins by understanding expected value, not by selecting a tool or writing a prompt.
3. Before acting, an agent must consult the current source of truth: code, tests, contracts, decisions, and repository instructions.
4. Architectural, contractual, economic, or security changes require an explicit decision before implementation.
5. Every delegation needs a goal, authorized scope, restrictions, acceptance criteria, and a clear stop condition.
6. Execution takes place in an isolated environment and produces a reversible change, preferably in its own branch or worktree.
7. No success claim replaces evidence: diffs, tests, static analysis, functional demonstration, and known limitations.
8. Review depth and autonomy must rise or fall with risk, impact, and reversibility.
9. Parallelism must be limited by the capacity to verify and integrate, not by the number of available agents.
10. Models, tools, and providers should be chosen for their fit to the task, considering capability, cost, privacy, and risk.
11. Relevant decisions, corrections, and lessons must return to the repository to reduce dependence on conversational memory.
12. The team must continually reduce technical debt, pattern drift, and entropy created by increased speed.

## 6. Roles and Responsibilities

C.H. defines responsibilities rather than fixed positions. In a small team, a person or agent may hold multiple roles, but human accountability must not be confused with agentic execution.

| Responsibility | Function in the method |
|---|---|
| **Human Owner** | Defines value, priority, acceptable risk, and final approval. Remains accountable for the product and cannot transfer that responsibility to AI. |
| **Cognitive Orchestrator** | Converts intent into decisions and W Slices, selects agents, bounds scope, identifies conflicts, and coordinates reviews. May be a person or a supervised AI. |
| **Agentic Executor** | Executes the W Slice in the authorized environment, modifies only permitted scope, and produces tests, diffs, documentation, and an execution report. |
| **Evidence Guardian** | Checks whether criteria were actually met, challenges assumptions, and evaluates security and coherence. Must be sufficiently independent of execution. |
| **Memory Maintainer** | Preserves instructions, maps, ADRs, contracts, standards, and lessons as a versioned source of truth. |

In Maestro Router, Hallan serves as Human Owner; ChatGPT primarily acts as Cognitive Orchestrator and architecture reviewer; Codex serves as Agentic Executor; and tests, ChatGPT review, and Hallan's approval together form the Evidence Guardian function. The repository itself, through versioned documents and decisions, sustains memory.

## 7. Essential Artifacts

| Artifact | Purpose |
|---|---|
| **Product Map** | Vision, problems, existing capabilities, limits, and intended evolution. |
| **W Slice Backlog** | Prioritized queue of W Slices; future ideas are not mistaken for existing capabilities. |
| **Decision Record** | ADR or equivalent note for decisions affecting contracts, architecture, economic policy, or security. |
| **Execution Contract** | Closed prompt or specification with baseline, permitted scope, prohibitions, criteria, and expected outputs. |
| **Evidence Package** | Diffs, tests, checks, demonstrations, hypotheses, limitations, costs, and deviation reports. |
| **Integration Request** | Draft PR or equivalent unit for review before incorporation. |
| **Acceptance Record** | Approval, rejection, or correction request from the accountable human. |
| **Versioned Memory** | Agent instructions, documentation, maps, standards, and technical history in the source of truth. |

