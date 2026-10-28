# Decision 004: request interpretation and workflow execution

Recorded: 2026-10-28. Status: agreed conceptual direction; naming, contracts, implementation and detailed coverage remain open.
Origin: user discussion of Java interfaces and multiple workflow flavours, followed by explicit agreement that the two independently variable boundaries make sense. This does not select a stack or authorize implementation.

## Context

The user is familiar with Java and somewhat with Python, with less familiarity with JavaScript, Ruby and shell/PowerShell scripting. Understandability, maintenance and extension by the user are important evaluation criteria. Java interfaces/APIs are candidates, not mandates.

The user's examples of AI assistants include GitHub Copilot, Codex, Gemini, Antigravity and Claude Code. These are examples of desired interaction possibilities, not verified integrations or interchangeable embedded runtimes.

## Agreed direction

Separate two independently configurable responsibilities, using provisional terminology:

1. Request interpretation: understand intent, resolve ambiguity and collect parameters.
2. Workflow execution: perform the explicit operation within its constraints and permissions.

Connect them through an explicit, inspectable operation request. It describes the intended operation; the executor is what performs it. Do not assign an implementation flavour to the request data itself. Candidate names include action/command, command/executor and interpreter/command/executor; defer final names to actual repository design/development.

Support non-AI, bounded-AI and agent-led variants where useful. Interpretation and execution may vary independently:

| Entry / interpretation | Execution example |
|---|---|
| Fixed command, menu or form | Deterministic retrieval and assembly |
| AI assistant interpreting a request | Deterministic search or standard recap without rewriting its result |
| Fixed command or UI action | Bounded AI recap using selected sources and output constraints |
| Agent-led clarification | A fixed workflow after intent is resolved |
| User-selected adaptive session | Agent-led revision using permitted capabilities |

An AI assistant may use an LLM to interpret an instruction even when the invoked operation is non-AI. An entirely non-AI path must also have an entry point that does not require an LLM. Bounded AI still produces variable results; control of workflow steps and the mechanism used for each step are separate dimensions.

Use a default per workflow with an explicit override. Mode selection should be visible, with no silent escalation from non-AI to AI. Automatic selection within configured rules is an explained future option, not a selected initial requirement.

All variants share applicable source boundaries, validation, identity, permission and review rules. An agent-led workflow may be read-only; deterministic code may modify files. Mode is not authorization. Preserve Decision 001's version-specific approval before proposed application and Decision 002's separate review/approval for commit/push. Generated output is not automatically accepted vault content.

## Recap example and initial recommendation

For a non-AI recap, initially retrieve/assemble accepted summaries, key points, examples and links using explicit rules. If suitable material is missing, report the limitation and offer existing notes; do not silently generate an answer. Deterministic extraction from arbitrary prose may lose qualifications and is not a promised synthesis capability. This recommendation was included in the explanation the user found sensible; exact content conventions and quality criteria remain open.

Bounded AI may generate a recap from selected sources under constraints. Agent-led revision may investigate and adapt within permissions. An AI-generated recap may be proposed for review and, if explicitly accepted/applied, become authored knowledge reusable by future non-AI workflows.

The user prefers complete non-AI workflows where possible but remains unsure of exact scope. Completeness of a user workflow does not imply identical synthesis or adaptation across modes. Do not promise three implementations of every capability.

## Design implications and open details

- Candidate capability contracts include finding notes, explaining from notes, preparing/conducting revision and proposing enhancements. These examples are not a selected interface catalog.
- Interchangeability requires shared behavioral guarantees, not just matching Java method signatures. An explanation without actual note references cannot satisfy a contract promising retrieved notes.
- Compose shared operations and vary individual steps where appropriate; avoid duplicating whole workflows solely for symmetry.
- A Java interface is an in-process contract, not automatically a remotely exposed API. HTTP/tool/CLI adapters, embedded versus external-agent control, and integration feasibility remain to be evaluated.
- Request schema, source/version references, validation, ambiguity handling, output presentation, error/partial-result handling, cancellation, privacy/cost limits and fallback behavior remain unselected.
- Language/runtime, Java libraries, modules, deployment and provider choices remain open. Java familiarity is a decision input, not an approved Java-only architecture.

## Traceability

Requirements U02, U05, U12 and U24–U28; inventory K10–K11, L01–L04, E01/E04/E16 and historical alternatives H01–H03.
Related: [Decision 001](001-import-review.md), [Decision 002](002-vault-platform-boundaries.md), [Decision 003](003-knowledge-navigation-and-review.md), [requirements](../../requirements/requirements-register.md), [open questions O12–O15](../../reviews/open-questions.md).
