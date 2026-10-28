# Open questions and review gates

Updated: 2026-10-28. These are recorded design questions, not unfinished publication tasks. No item below blocks the user's next question/concern. Formal design/implementation gates remain explicit.

| ID | Question / unresolved detail | Status / next treatment |
|---|---|---|
| O01 | Exact folder taxonomy, whether one primary parent is mandatory, relationship semantics and note identity/link preservation through moves | Open; primary-parent direction provisional; test real notes before selecting structure |
| O02 | Metadata fields, conditional requirements, format/location, generated versus inferred values and review rules | Open; mandatory/optional distinction desired, no schema selected |
| O03 | Finalization thresholds and which validation issues, if any, block platform commit/push; enforcement outside the platform | Open; retain readable content and offer reviewed repairs; no blanket blocking rule approved |
| O04 | Ordinary revision conversations leave the vault unchanged and offer enhancements | Provisional default; revisit examples, not a permanent silent-capture policy |
| O05 | Offline/unavailable-vault capture and pending overlap assessment | Assistant proposal awaiting later confirmation; avoid promising duplicate prevention without retrieval |
| O06 | Derived-view fallback representation, freshness, refresh/commit policy and dynamic navigation UI | Open; dynamic views plus readable fallback agreed in principle |
| O07 | Learning-path representation and ordering versus query-generated sections | Both behaviors desired; mechanics open |
| O08 | Phone offline reading/search scope, downloaded subset, refresh and synchronization experience | Explicitly unanswered; priorities already recorded in Decision 002 |
| O09 | Notion/Confluence editing feasibility, identity/version mapping, fidelity and reconciliation | Desired early capability; technical investigation pending |
| O10 | Detailed concurrency/conflict handling, rollback, interrupted/failed application and proposal persistence | Open; preserve conflicts and interrupt for review accepted for now |
| O11 | Privacy/local-cloud boundaries, backups/restore guarantees, accessibility/performance and search/learning quality criteria | Open; derive measurable expectations from use cases |
| O12 | Runtime/language, modules, agent/tool composition, deployment and migration dispositions | Open; Decision 004 clarifies conceptual boundaries only; no implementation architecture chosen |
| O13 | Final naming, operation-request schema, capability guarantees and composition of interpreter/executor variants | Open; conceptual separation agreed in Decision 004 |
| O14 | Which workflows have complete non-AI variants, recap content conventions, quality limits and behavior when required material is absent | Open; existing-material assembly is the initial recommendation, no parity promise |
| O15 | Concrete assistant integrations/access adapters, mode overrides, future routing rules, budgets, error/cancellation and fallback behavior | Open; no provider/transport selected; no silent AI escalation |
| O16 | Whether historical shared-workspace, collaborative editing/annotation and sharing capabilities belong in successor scope | Candidate only (K02/K14/E07; BLI-077/079); preserve ideas, no multi-user or sharing approval |

## Remaining review gates

- Formal inventory-coverage confirmation remains pending; targeted gaps can be investigated during ongoing questions.
- Continue requirements/questions iteratively, then review a starting draft design.
- Obtain explicit authorization before creating the implementation repository/vault, scaffolding code or configuring IntelliJ.

## Completion accounting

Repository boundaries and planning migration are completed. Migration pointer PR [94](https://github.com/saharshpoddarorg/learning-assistant/pull/94) was merged at 73bfb9caeefaba3c06cb1ac4362f0fd9ff8e6804. Historical evidence remains at the pinned origin.

This register preserves unanswered questions rather than requiring premature decisions. Add answers with rationale and affected requirement/decision IDs; keep superseded reasoning recoverable.

## Holistic review follow-up

[Review findings](2026-10-28-holistic-review.md) and the [candidate supplement](../discovery/candidate-detail-supplement.md) preserve compressed historical detail. Their inclusion does not create implementation tasks or resolve the open questions above. Planning PR 1 is merged; the review changes use a separate PR.
