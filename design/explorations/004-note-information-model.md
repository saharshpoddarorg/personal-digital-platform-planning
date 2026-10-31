# Minimal note information model

Recorded: 2026-10-31. Status: starting design proposal, not an approved schema or implementation.

## Stage and discussion status

Conceptual architecture design is already underway: workflow responsibilities, identity, review boundaries and now information modeling. Detailed format/API/module design follows review of these proposals; implementation still requires explicit authorization. The user asked to continue with the assistant's best starting point, while remaining unsure about metadata granularity. Whole-note metadata first is therefore a provisional recommendation, not a settled requirement. Section metadata remains a possible later extension.

The user also reiterated liking conservative pause/show-differences behavior even for apparently unrelated edits, while remaining unsure. U30 stays provisional; evaluate interruption cost with examples rather than treating this as final policy.

## Conceptual information groups

| Group | Information | Authority / ownership |
|---|---|---|
| Authored note | Stable identity, readable title, body, applicable descriptions, explicit relationships and citations | Canonical knowledge, portable independently of the platform |
| Observed source | Current location, exact observed version and retrievable base where required | Observed from actual source; not a second manually maintained note description |
| Derived views | Backlinks, child listings, reverse path membership, search index and freshness information | Rebuildable from sources; generated views are not another canonical copy |
| Capture material | Original input, context and pending overlap/enrichment work | Not automatically finalized knowledge |
| Change proposal | Base/source versions, item versions, additions/modifications/removals, dependencies, preview and review state | Separate from note knowledge status; application requires authorization |
| Learning session | Questions, answers, recap and current-session adaptation | Separate from optional durable progress; retention policy remains open |

These are distinctions of meaning, not six databases, classes or repositories. No serialization, storage topology or universal object hierarchy is selected.

## Three representative notes

| Information | Java memory model | Strategy pattern | Interview preparation |
|---|---|---|---|
| Identity | Stable note identity | Different stable identity | Different stable identity |
| Title | Java memory model | Strategy pattern | Interview preparation |
| Body | Explanation, examples, limitations | General explanation plus language-specific examples | Goal, guidance and ordered references |
| Concepts | Concurrency, memory visibility | Design patterns, interchangeable behavior | Interview preparation |
| Programming-language applicability | Java; finer JVM/version applicability requires review | Optional for the general note; examples identify their language | Not required merely because it links to Java notes |
| Relationships | Related notes, citations, proposed prerequisites where useful | Related patterns and citations | Ordered path membership linking existing notes |
| Derived information | Incoming links, paths referencing it, search entries | Incoming links and relevant collections | Reverse membership on referenced notes |

Examples illustrate structure, not verified teaching content, a selected taxonomy or an exhaustive metadata list. A path may be represented by a note with structured entries; it does not yet require a separate storage entity. If a path contains dynamic sections, keep authored ordering distinct from query relevance and expose what was selected at execution time.

## Minimal versus conditional information

Starting candidates for finalized notes are a stable identity and an identifiable title. Derive the display title from an agreed source such as a heading where possible, rather than require duplicate typing. The exact title source, uniqueness rules and identity assignment flow remain open. A missing ID/title must not make manual captures or existing files disappear; retain read access and offer reviewable repair before operations requiring stable identity.

Other fields should justify their cost:

- Concepts/tags help retrieval but a mandatory vocabulary is not selected.
- Programming language applies only where meaningful. Do not equate prose language, implementation example language, Java API applicability and JVM-wide concepts.
- Versions are conditional when content actually depends on a runtime/library version. Do not add empty version fields to all notes.
- Citations/provenance should describe actual sources; an unsupported inference must not invent provenance.
- Difficulty, mastery, review dates and learning schedules are optional candidates. User-specific mastery belongs to learning progress, not an intrinsic universal property of a note.

There is no blanket finalization or commit-blocking schema approved. O02/O03 govern the remaining field and enforcement choices.

## Relationships with clear meaning

| Relationship | Proposed meaning | Derived counterpart |
|---|---|---|
| Related to | Explicit useful connection, without asserting teaching order | Incoming references; symmetric presentation can be derived if chosen |
| Prerequisite | A directed claim that one topic helps prepare for another | Topics that depend on this one |
| Path membership | An ordered reference owned by a learning path | Paths that include this note |
| Parent / child | A navigation relation, if adopted | Child listing from the chosen authoritative parent/folder representation |
| Citation | Evidence/source reference | Optional source usage view, not an ordinary topic relationship |

Do not store independently editable lists on both sides of one fact. For parent navigation, choose an authoritative representation later: folders, explicit parent metadata or another reviewed convention. Do not silently require the folder tree and a parent field to mirror each other. One primary parent remains provisional.

Expandable navigation must eventually handle cycles, missing references and repeated nodes without infinite traversal or duplicated canonical content. Cycle constraints differ by relationship: related-note cycles can be useful; a strict parent tree cannot contain them. Exact validation and rendering are open.

## Authored versus inferred versus derived

Authored/accepted metadata expresses meaning the user intends to preserve. Inferred metadata is a suggestion with evidence and uncertainty until reviewed. Derived metadata is computed from explicit sources, such as backlinks; it need not demand approval every time it is displayed. Writing a generated fallback into canonical files is a separate effect whose authorization and refresh rules remain unresolved under O06.

Use a section heading such as “Java example” inside a general Strategy pattern note initially. Do not automatically label the entire concept Java-only because one code block uses Java. Introduce section metadata only when precise section retrieval, applicability or independent review justifies durable anchors and additional editing complexity.

## Stress cases to review

- A handwritten note has no metadata: it stays readable and discoverable, with issues surfaced and repairs offered.
- An accepted note acquires a metadata problem: keep it in place; mark the issue/change for review.
- The same note appears in two paths: maintain one body and two references.
- A folder move disagrees with explicit parent metadata: expose the ambiguity; first decide which representation is authoritative.
- An inferred concept tag is wrong: allow correction without confusing the suggestion with accepted knowledge.
- A note changes during review: pause and show differences under provisional U30, preserving unaffected review history and checking dependencies.
- A dynamic view is unavailable: show useful authored context and readable fallback, with freshness limits disclosed.

These are proposed design checks, not runtime tests. No schema or platform behavior has been implemented.

## Next session

Review these groups and three examples. Then compare folder-derived hierarchy with explicit parent relationships and decide the smallest useful metadata set. Ask focused questions only where a choice changes the user experience; do not repeatedly seek permission for routine drafting. After those semantics are sufficiently clear, propose concrete request/result contracts and evaluate formats/modules. No need to repeat the audit or perform the optional tool trial.

Traceability: U03/U10–U13/U16–U22/U24/U29/U30; K03–K11/K15, L02/L04/L05; O01–O03/O06/O07/O10/O11/O13/O17. See [requirements](../../requirements/requirements-register.md), [identity exploration](002-note-identity-and-versioning.md), [workflow draft](001-workflow-architecture-draft.md), [tooling direction](003-personal-project-tooling.md) and [open questions](../../reviews/open-questions.md). No historical capability has been silently removed or approved for implementation.
