# Candidate detail supplement

Reviewed: 2026-10-28. Status: historical candidates, not accepted requirements.

The original 62 groups are deliberately broad. This supplement makes under-explicit details discoverable without multiplying capability IDs or implying new scope. Recover full descriptions, acceptance criteria and future considerations from the pinned sources. See the [crosswalk](source-capability-crosswalk.md) for source accounting.

## K08 / K11 — classification and vocabulary lifecycle

Structured multi-value labels versus free-form tags; synonym/case normalization; tag namespaces and co-occurrence; vocabulary governance; technology/person/concept entity extraction; confidence, reviewed suggestions, correction feedback and reclassification when vocabulary or algorithms change. Programming-language applicability and the natural language of content are distinct dimensions. None selects enums, NLP algorithms or automatic application.

Evidence: [BLI-080](https://github.com/saharshpoddarorg/learning-assistant/blob/8db1797ef36ef68f6675ad53231f887d51fd92b9/brain/ai-brain/backlog/features/BLI-080_search-engine-labelling-system.md), [BLI-081](https://github.com/saharshpoddarorg/learning-assistant/blob/8db1797ef36ef68f6675ad53231f887d51fd92b9/brain/ai-brain/backlog/features/BLI-081_search-engine-tagging-system.md), [BLI-084](https://github.com/saharshpoddarorg/learning-assistant/blob/8db1797ef36ef68f6675ad53231f887d51fd92b9/brain/ai-brain/backlog/features/BLI-084_search-engine-auto-classification-entity-extraction.md).

## K11 — retrieval usability and index maintenance

Search history, saved queries/filter presets, facet counts, nested/relative-date facets, multi-field indexes, incremental rebuilds, stemming/language analysis, index compaction/snapshots, source authority/media preferences and current-to-target learning levels. Preserve query-level AND/OR choices as proposals rather than assuming one global rule. Old numerical performance targets and library choices are not adopted.

Evidence: [BLI-075](https://github.com/saharshpoddarorg/learning-assistant/blob/8db1797ef36ef68f6675ad53231f887d51fd92b9/brain/ai-brain/backlog/features/BLI-075_search-engine-online-local.md), [BLI-082](https://github.com/saharshpoddarorg/learning-assistant/blob/8db1797ef36ef68f6675ad53231f887d51fd92b9/brain/ai-brain/backlog/features/BLI-082_search-engine-full-text-indexing.md), [BLI-083](https://github.com/saharshpoddarorg/learning-assistant/blob/8db1797ef36ef68f6675ad53231f887d51fd92b9/brain/ai-brain/backlog/features/BLI-083_search-engine-metadata-index-faceted-search.md), [BLI-087](https://github.com/saharshpoddarorg/learning-assistant/blob/8db1797ef36ef68f6675ad53231f887d51fd92b9/brain/ai-brain/backlog/features/BLI-087_learning-resources-taxonomy-enum-sso.md).

## K02 / K14 / E07 — sharing and collaboration

Shareable Markdown/HTML/PDF outputs, shared workspaces/collaborative editing and collaborative annotations were historical future ideas. Existing inventory groups preserve sharing broadly but do not make multi-user collaboration obvious. These are candidates to evaluate, not permission to share private notes or requirements for initial delivery.

Evidence: [BLI-077](https://github.com/saharshpoddarorg/learning-assistant/blob/8db1797ef36ef68f6675ad53231f887d51fd92b9/brain/ai-brain/backlog/features/BLI-077_pkm-brain-notes-manager.md), [BLI-079](https://github.com/saharshpoddarorg/learning-assistant/blob/8db1797ef36ef68f6675ad53231f887d51fd92b9/brain/ai-brain/backlog/features/BLI-079_presentation-of-information.md).

## E07 — response presentation contracts

Request-intent-specific response structure, verbosity/depth overrides, code-first versus prose-first output, generated tables of contents, diagrams and exportable presentations. Historical alternatives include a central instruction section, dedicated instruction file or per-skill rules. The old source recommends collecting concrete pain points before adding rules; no old formatting policy is adopted.

Evidence: [BLI-079](https://github.com/saharshpoddarorg/learning-assistant/blob/8db1797ef36ef68f6675ad53231f887d51fd92b9/brain/ai-brain/backlog/features/BLI-079_presentation-of-information.md), [BLI-088](https://github.com/saharshpoddarorg/learning-assistant/blob/8db1797ef36ef68f6675ad53231f887d51fd92b9/brain/ai-brain/backlog/items/BLI-088_output-format-response-structure-rules.md).

## E05 / H01–H03 — staged cross-assistant portability

Manual sync plus review, canonical-source templates, validation-only tooling and a full transpiler are distinct alternatives. A staged validation/drift → selective generation → possible compiler path was discussed historically. Preserve unsupported primitive warnings, dry-run create/update/skip reporting, idempotence and versioned profile contracts. Portable customization content is separate from invoking an assistant as a runtime executor (Decision 004); tool-specific claims need verification.

Evidence: [BLI-090](https://github.com/saharshpoddarorg/learning-assistant/blob/8db1797ef36ef68f6675ad53231f887d51fd92b9/brain/ai-brain/backlog/items/BLI-090_universal-ai-customization-framework-epic.md), [BLI-092](https://github.com/saharshpoddarorg/learning-assistant/blob/8db1797ef36ef68f6675ad53231f887d51fd92b9/brain/ai-brain/backlog/items/BLI-092_design-tool-agnostic-abstraction-layer.md), [BLI-103](https://github.com/saharshpoddarorg/learning-assistant/blob/8db1797ef36ef68f6675ad53231f887d51fd92b9/brain/ai-brain/backlog/items/BLI-103_implement-deterministic-sync-adapters.md), [BLI-104](https://github.com/saharshpoddarorg/learning-assistant/blob/8db1797ef36ef68f6675ad53231f887d51fd92b9/brain/ai-brain/backlog/items/BLI-104_define-tool-profile-specs-and-antigravity-mapping.md).

## E06 / K14 / G10 — environment recovery

Workspace backup/restore, dependency/config validation, cross-OS migration and deciding what to copy versus regenerate extend beyond document export. Credential handling is a separate unresolved concern; the historical suggestion to bundle API keys is not adopted and no credentials were read or copied.

Evidence: [BLI-022](https://github.com/saharshpoddarorg/learning-assistant/blob/8db1797ef36ef68f6675ad53231f887d51fd92b9/brain/ai-brain/backlog/features/BLI-022_export-migration-portability.md).

## K09 / L05 / L06 / G01 — knowledge-learning feedback

Every resource reachable through navigation, notes/sessions linked to resources, learning-path completion recorded and recommendations informed by studied material. These are candidates already distributed across multiple inventory groups, not a verified learner-state implementation.

Evidence: [BLI-003](https://github.com/saharshpoddarorg/learning-assistant/blob/8db1797ef36ef68f6675ad53231f887d51fd92b9/brain/ai-brain/backlog/features/BLI-003_module-hierarchies-learning-resources.md), [BLI-004](https://github.com/saharshpoddarorg/learning-assistant/blob/8db1797ef36ef68f6675ad53231f887d51fd92b9/brain/ai-brain/backlog/features/BLI-004_brain-integration-learning-resources.md).

## E04 / K13 — workflow generation from discovery

The old source proposes suggesting new prompts/skills when discovery exposes a new domain, and maintaining composition recipes and framework fitness reviews. Preserve as candidate tooling ideas; this does not authorize automatic creation or adoption of old primitive counts and layering.

Evidence: [BLI-012](https://github.com/saharshpoddarorg/learning-assistant/blob/8db1797ef36ef68f6675ad53231f887d51fd92b9/brain/ai-brain/backlog/features/BLI-012_enhanced-web-scraping-search-engine.md), [BLI-026](https://github.com/saharshpoddarorg/learning-assistant/blob/8db1797ef36ef68f6675ad53231f887d51fd92b9/brain/ai-brain/backlog/features/BLI-026_evolve-6-primitive-layered-architecture.md).
