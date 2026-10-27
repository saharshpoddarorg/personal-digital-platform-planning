# Decision 003: knowledge navigation, metadata and review

Recorded: 2026-10-27. Origin: user discussion following Decision 002.
Status: mixed; agreed directions, provisional preferences and unselected proposals are identified below. This record does not approve a metadata schema or implementation design.

## User needs and agreed directions

- Initial content is mainly career-oriented/software-engineering learning; allow other personal learning, notes and finance topics without treating their detailed scope as approved.
- Support hierarchical navigation expandable through descendants to leaf notes. Parent pages should combine navigation with a short overview and optional learning guidance. The user mentioned tree/graph navigation; exact graph semantics and UI are unselected.
- Support different browsing, searching, learning, revising and editing routes to the same knowledge. Metadata, relationships, indexes and retrieval may be processed by deterministic code; these capabilities need not be AI-driven.
- Support both explicitly ordered learning paths and automatically discovered material. Query relevance alone does not prescribe pedagogical order.
- Some metadata should be mandatory and some optional; applicable conditional requirements are useful. Exact fields, schema, format and enforcement stages remain open. The user's XML example illustrates programming-language applicability (Java/JDK versus JVM-wide relevance), not the language of the prose. It is not an approved serialization format.
- Keep content accessible when metadata is missing or invalid. Flag issues, infer/suggest values where appropriate, and offer repairs for review rather than silently applying them or hiding content.
- Allow quick capture as inbox material, with review, enhancement/enrichment and commit/push later. Before knowledge integration, check existing/related material and avoid redundant additions. Propose enhancement of an existing note when genuinely useful information is added.
- Resolve applicable missing or irrelevant information before finalization as far as possible; unfinished new material may remain pending/inbox. Exact finalization thresholds remain open; this does not require every optional field to be populated.
- Existing accepted notes remain in their canonical location when edits need review. Mark the changes/issues as needing review; do not downgrade or move the note to the inbox because of a metadata problem. Note location, knowledge status and change-review status are distinct concerns, not yet an implemented state machine.
- Decision 001's proposal-version/application review and Decision 002's commit/push approval boundaries continue to apply.

## Examples and rationale

Strategy pattern revision: if existing design-pattern notes already cover the answer and the discussion adds no useful knowledge, do not create another note. If it adds a useful explanation or example, propose an enhancement to the existing material. New capture does not imply acceptance into finalized knowledge.

Java memory model: a single note may be discoverable through concurrency concepts, Java applicability and an interview-preparation path. Suggested separation: hierarchy supplies a primary browsing location; metadata describes the note; relationships express connections; derived indexes retrieve/display them. The exact schema remains unselected.

Suggested relationship direction: a learning path references its members and a reverse 'included in these paths' view is derived. Distinguish source citations, related notes, prerequisites and path membership rather than overloading an ambiguous references field. These are design proposals, not a finalized relationship model.

## Provisional preferences and proposals

- One primary parent with links/derived collections elsewhere is plausible to the user ("not sure but makes sense"); one canonical copy remains the working preference from Decision 002. A strict parent constraint and folder taxonomy are not approved.
- Ordinary learning/revision conversations leave the vault unchanged by default, with useful enhancements offered for review: accepted only for now ("not sure, but makes sense for now"). Revisit using examples.
- Required information need not require manual typing. Generated identity, inferred titles and proposed classification are candidate approaches; the exact fields and review policy remain open.
- A folder containing index.md is an illustrative representation only, not a selected convention.
- When quick capture occurs without access to existing knowledge, preserving input and marking overlap assessment pending was proposed by the assistant; the user has not explicitly settled this fallback.
- Preventing platform commit/push on metadata errors is not approved. The user favored review/repair and pending status; distinguish critical and optional issues before deciding blocking rules. External editors/direct Git can bypass platform validation unless separate enforcement is chosen.

## Open questions

Tracked as O01–O07 in the [open-question register](../../reviews/open-questions.md). No answer is required before the user's next concern. Do not silently resolve these questions while implementing unrelated work.

## Traceability

Requirements U03, U11–U12, U16–U23; inventory K03, K05–K11, K15 and G08/G11; learning L04/L05.
Related: [Decision 001](001-import-review.md), [Decision 002](002-vault-platform-boundaries.md), [requirements](../../requirements/requirements-register.md).
