# Requirements register

Status: discovery baseline, not a finalized SRS.
Accepted preferences below still need measurable acceptance criteria.
No new-platform implementation or test coverage is claimed.

## Confirmed direction and boundaries

| ID | Record | Status / origin |
|---|---|---|
| U01 | Long-lived Personal Digital Platform; PKM and Learning first; Productivity and Planning evolve from real need. | User context transfer |
| U02 | Manual editing and platform-driven creation/import/organization/linking/enhancement via deterministic code/APIs, configured flows or AI agents. | Accepted mechanism-independent scope; Decision 002 |
| U03 | Rich navigation, metadata, tags, relationships and lexical/semantic/AI retrieval. | User preference; implementation open |
| U04 | Desktop and Android, portability, privacy, backups, longevity. | User preference; measurable requirements pending |
| U05 | Learn software engineering through iterative architecture discussion and pair programming. | User preference |
| U06 | Existing repo is reference and evidence, not approved architecture; intentional review of retained/removed/rebuilt ideas. | Explicit user instruction |
| U07 | Complete extraction -> user confirms coverage -> further brainstorming/questions -> starting draft design -> authorization before new repo/IntelliJ/implementation. | Explicit user sequence |
| U08 | Save extraction and decision references for future design. | Initially stored through learning-assistant PR #91; active records migrated to personal-digital-platform-planning with user authorization on 2026-10-27 |
| U09 | User will later create a separate repository named personal-digital-platform for the reviewed redesign. learning-assistant remains reference material, not an inherited architecture. | Explicit clarification, 2026-10-27; creation/implementation not yet authorized |
| U10 | Independent Git repositories for the platform and canonical vault; configured vault location and usability without the platform. | Accepted planning direction, 2026-10-27; Decision 002; creation not authorized |
| U11 | Authored knowledge plus dynamic derived views with readable fallbacks; underlying notes understandable without macros. | Agreed in principle; refresh/storage policy open |
| U12 | Manual local edits or explicitly authorized proposal application; commit/push requires review and explicit approval independently of permission to edit/apply. | Accepted rules, 2026-10-27; Decisions 001/002 |
| U13 | Preserve originals, expose meaningful conversion loss and resolve it explicitly; preserve conflicting edits and interrupt for review. | Loss rule accepted; conflict handling accepted for now, mechanics open |
| U14 | Notion/Confluence editing desired early with reconciliation into the authoritative vault. | Desired capability, not initially required; feasibility/fidelity open |
| U15 | Phone reading/search, remote refresh and inbox capture precede proposal review, finalized-note editing and commit/push actions. | User priority; offline-search scope open |
| U16 | One canonical note with links from elsewhere; folder-like navigation. | Working preference; exact organization open |
| U17 | Expandable descendant navigation to leaf notes, with parent overview and optional learning guidance; multiple retrieval/browsing routes. | User requirement direction; exact tree/graph UI open |
| U18 | Support explicitly ordered learning paths and automatically discovered material. | User preference confirmed; representation open |
| U19 | Mandatory/optional and applicable conditional metadata; inferred values and repairs reviewable, content stays accessible. | Agreed direction; schema/enforcement open |
| U20 | Quick capture may remain inbox material for later review/enrichment and approved commit/push. Check existing knowledge before integrating; enhance rather than duplicate useful existing material. | Agreed behavior; unavailable-vault overlap fallback not settled |
| U21 | Existing notes with problematic edits remain in place; changes/issues need review rather than moving accepted notes to inbox. | Explicit user agreement |
| U22 | Ordinary revision conversations leave the vault unchanged by default while offering useful enhancements. | Provisional only; user remains unsure |
| U23 | Initial emphasis on career/software-engineering learning, with possible personal learning, notes and finance topics. | User scope preference; broader domain detail open |
| U24 | Separate request interpretation from workflow execution, connected by an explicit operation request; variants can be chosen independently. | Agreed conceptual direction, 2026-10-28; Decision 004; naming/contracts open |
| U25 | Support non-AI, bounded-AI and agent-led approaches where useful; an AI entry point can invoke a non-AI operation. | Agreed direction; no requirement for three implementations of every capability |
| U26 | Default mode per workflow with explicit override; visible selection and no silent escalation to AI. | Agreed direction; automatic rule-based selection not selected |
| U27 | Prefer complete non-AI workflows where feasible; initially assemble existing recap material and disclose missing content rather than promise arbitrary synthesis. | User preference and initial recommendation; exact coverage and quality criteria open |
| U28 | Evaluate technology for user understandability/maintenance; Java familiarity matters without mandating Java-only implementation. | User preference; stack selection open |

## Traceability

- U02 maps to inventory K01–K07 and review behavior R01–R10.
- U03 maps to K08–K11.
- U04 affects all domains; offline, privacy, backup and performance targets remain unspecified.
- U06–U07 map to G06–G08 and the completeness-review gate.
- U10–U16 map to [Decision 002](../design/decisions/002-vault-platform-boundaries.md), which links related inventory IDs and historical alternatives.
- U17–U23 map to [Decision 003](../design/decisions/003-knowledge-navigation-and-review.md); unresolved details are in the [open-question register](../reviews/open-questions.md).
- U24–U28 map to [Decision 004](../design/decisions/004-workflow-interpretation-and-execution.md), E04/E16 and open questions O12–O15.
- Inventory candidates are not automatically accepted requirements.

## Deferred questions

- Initial concrete use cases and success criteria; product scope versus adjacent experiments.
- Agent count and orchestration; skill composition versus delegation; PKM/Learning overlap.
- Detailed vault representation, internal module organization, deployment and technology stack. Separate platform/vault Git repositories and canonical vault ownership are accepted in Decision 002; names/hosting beyond personal-digital-platform remain open.
- Manual editing, source retention, provenance, re-import, contradiction handling and cross-device concurrency.
- Granular review dependencies, rollback, interrupted/failed application and review persistence.
- Privacy boundaries, local/cloud processing and integration feasibility.
- Search quality/evaluation, learning progress/assessment and revision behavior.
- Backup/restore expectations, offline behavior, portability and accessibility.
- Which existing pieces to retain/refactor/merge/redesign/migrate/defer/intentionally remove.

See [inventory](../discovery/source-inventory.md), [review agreement](../design/decisions/001-import-review.md)
and [checkpoint](../reviews/current-checkpoint.md).
