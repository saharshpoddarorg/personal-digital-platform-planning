# Note identity, navigation and reviewed versions

Recorded: 2026-10-31. Status: proposal for iterative review; no identity schema, link syntax or concurrency implementation is approved.

## Problem and recommendation

A canonical note may appear in several navigation routes, move between folders, and be edited manually while a platform proposal awaits approval. Neither a path alone nor a Git commit alone describes all these situations.

Propose separating stable note identity, current location and exact observed version. Use the identity across platform capabilities and retain ordinary readable links for independent vault use. A platform-managed lookup index should be rebuildable from portable vault information, rather than being the only place identities survive.

The user authorized continuing design, not acceptance of the alternatives below. This extends the [workflow draft](001-workflow-architecture-draft.md) without selecting Java interfaces or repository layout.

## Distinct concepts

| Concept | Purpose | Illustrative value, not a schema |
|---|---|---|
| Vault identity | Scope note identities when multiple vaults or copies exist | personal knowledge vault |
| Note identity | Refer to the same note despite title/path changes | note-123 |
| Location | Locate its current editable representation | learning/java/memory-model.md |
| Observed version | Identify exactly what was read or reviewed, including uncommitted content | content fingerprint plus retrievable snapshot |
| Git revision | Explain committed history or remote publication state | commit reference, when available |
| Proposal/item version | Identify the particular suggested changes and subset approved | proposal P, item 2, revision 3 |

Names and example values are explanatory. No identifier algorithm, serialization or metadata field list is selected. A fingerprint detects differences; it does not retain the old content needed for a comparison. Proposal recovery therefore needs access to the reviewed base, not only its fingerprint. Attachment and relationship dependencies may also need version references when they affect the proposal.

## Identity alternatives

| Approach | Advantage | Cost / limitation |
|---|---|---|
| File path as identity | Simple, human-readable, naturally usable in ordinary editors | Moves change identity; relationships and pending proposals must track path changes |
| Stable ID in portable note metadata | Identity travels with a moved file; lookup can be rebuilt | Copies can duplicate IDs; format and editor compatibility need evaluation |
| Stable ID in a separate manifest | Keeps note text free of identity metadata | Note and manifest can diverge on manual moves/copies; additional reconciliation |
| Identity only in a platform database | Convenient internal lookup | Loses independent portability unless separately exported; not recommended as the sole authority |

Starting recommendation: stable IDs persisted with notes, with an index derived from them. This is a candidate to evaluate against chosen formats/viewers, not approval of YAML, Markdown or any particular product. Scope IDs to a vault and distinguish another checkout of that vault from an intentionally independent fork; exact fork behavior remains open.

Missing metadata must not hide content. A newly hand-created note can be read by path and flagged for identity assignment before an operation requiring durable identity. Propose repairs; do not silently edit it. If copied files share an ID, show the ambiguity and pause identity-dependent mutation rather than selecting one arbitrarily. Copy-as-new should receive a distinct identity through the eventual approved editing flow.

## Walkthrough 1: move a note without duplicating knowledge

The Java memory model note is stored in one location and discovered through a Java folder, a concurrency collection and an interview learning path. These are different references or views of one note, not three copies. Folder hierarchy, conceptual relationships and learning order remain separate.

A move from one folder to another preserves the proposed note ID. The derived lookup updates its location after observing the change. Search and platform relationship resolution can find the new location without inventing a new note.

However, a stable ID alone does not fix ordinary relative links in an independent viewer. Proposed compatibility approach: retain readable file links, and use identity information to detect or propose repairs when targets move. Exact link representation is open. A platform-assisted move can preview the move and affected link edits together for authorization; an external manual move may leave links broken until reviewed repair. Do not promise automatic portability across every editor.

Do not use title similarity alone to redirect a missing note. Preserve unresolved references and show the issue. Deletion, splitting or merging notes requires explicit relationship/proposal reconciliation; a stable ID does not make those operations equivalent to a simple rename. Section anchors can also break when headings change; stable section IDs are a separate complexity, deferred until justified.

## Walkthrough 2: manual edit during proposal review

1. The platform reads note N at version V1 and prepares proposal P1 with independently reviewable items, its base snapshot and dependencies.
2. The user reviews a combined preview and authorizes a specific subset of P1 for application.
3. Before application, a manual edit creates V2. The Git commit may still be unchanged because this edit is uncommitted.
4. The platform re-reads affected notes and dependencies. V2 differs from the reviewed base, so it stops that application and shows the intervening change.
5. It may prepare a reconciled proposal P2 against V2, preserving manual content. Changes affecting approved portions require renewed review and explicit application authorization for the revised result. Disjoint approvals are not silently discarded, but their applicability and dependencies must be revalidated.
6. Only the authorized result is applied. Commit/push remains separately authorized under Decision 002.

Starting recommendation: check whole affected-note versions, not only changed lines. This is easier to reason about but may interrupt for a harmless edit elsewhere in the same note. Later, section-aware reconciliation may reduce interruptions if it preserves context and approval guarantees. Do not infer semantic safety merely because textual hunks do not overlap.

An unchanged move can preserve content identity, but the new target path and link/dependency effects must still be resolved before applying. A previously reviewed deletion or new-note creation also needs preconditions: absence, presence and identity must match expectations, not just file bytes.

A version check followed by a write has a race if another editor writes between them. This proposal defines the required behavior, not a complete solution. Implementation design must evaluate conditional writes, coordination with external editors, snapshots/recovery and multi-file failure handling. A platform lock alone does not control unrelated editors; an atomic file replacement alone does not prevent overwriting a concurrent change. Until a defensible mechanism is reviewed, do not claim conflict-free or atomic multi-note application.

## Read freshness is separate from write approval

A read result should identify the observed source version and any known index lag. Local freshness and remote freshness are different: a current local index may still describe an old clone. Offline or unchecked remote status should be shown as unknown, not current.

For revision, propose using the retrieved snapshot for a coherent session and offering refresh if changes are detected. A refreshed source may affect generated explanations/questions; do not silently mix versions while presenting one consistent source. This snapshot policy remains proposed; source availability and retention are open.

For proposal application, derived search results are insufficient proof of the current target state. Re-read the source and check relevant preconditions. A successful operation should report resulting versions and effects so a later retry can distinguish an already-applied change from an unapplied proposal; exact retry/idempotency mechanics remain O10.

## Implications for capability contracts

- Retrieval returns note identity, observed location/version, evidence and freshness limitations where known.
- Navigation resolves references to the same canonical note; multiple routes do not imply copies.
- Revision consumes cited source versions without requiring persistent learner progress.
- Enhancement produces versioned proposals with retrievable base content and dependency information.
- Application validates identity, version, selected proposal items and authorization at the write boundary.
- Publication reports local/remote Git state separately from note acceptance and proposal application.

These are contract information needs, not a final universal response type or six new modules. External connectors will need explicit identity/version mappings rather than assuming a Notion/Confluence page ID equals a vault note ID.

## Proposed review scenarios

| Scenario | Expected behavior to evaluate |
|---|---|
| Rename/move with unchanged note ID | Resolve same note; detect ordinary link repairs and location effects |
| Two files with one ID | Keep both readable; report ambiguity; block ambiguous mutation |
| Same title on distinct notes | Keep identities distinct; clarify ambiguous selection |
| Uncommitted manual edit after review | Detect base mismatch despite unchanged Git commit; reconcile before apply |
| Non-overlapping manual edit | Start conservatively with reconciliation; do not silently assume approval covers the new combined result |
| Deleted/replaced target or changed dependency | Pause affected application and preserve proposal for review |
| Remote cannot be checked | Report unknown remote freshness; do not imply latest hosted content |
| Failure or retry after partial application | Report actual effects and preserve recovery evidence; no duplicate application claim without a mechanism |

These are design review scenarios, not implemented or executed tests.

## Next focused decision and traceability

Review two recommendations before selecting schema or APIs: stable identity independent of location, and conservative re-review when affected source versions change. Then examine the minimum portable metadata/relationship model using real note examples. Existing O01/O02/O06/O09/O10/O11/O13 remain open.

Traceability: U10–U13, U16–U21 and U24; inventory K04/K05/K08–K11/K15/K17; [Decision 001](../decisions/001-import-review.md), [Decision 002](../decisions/002-vault-platform-boundaries.md), [Decision 003](../decisions/003-knowledge-navigation-and-review.md), [requirements](../../requirements/requirements-register.md) and [open questions](../../reviews/open-questions.md). No historical feature disposition or accepted requirement is changed.
