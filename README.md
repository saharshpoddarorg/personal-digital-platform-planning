# Personal Digital Platform — discovery and design records

Status: discovery baseline; not a finalized SRS or approved implementation architecture.
Updated: 2026-10-31.

This repository is the authoritative planning record for the Personal Digital Platform.
[learning-assistant](https://github.com/saharshpoddarorg/learning-assistant) is an experimental reference, not the architectural authority.
PKM and Learning are initial priorities; Productivity and Planning are future candidates.

## Read in this order

1. [Current checkpoint](reviews/current-checkpoint.md) — progress and pending reviews.
2. [Idea and capability inventory](discovery/source-inventory.md) — 62 groups with stable IDs and evidence; see also the [source crosswalk](discovery/source-capability-crosswalk.md) and [candidate detail supplement](discovery/candidate-detail-supplement.md).
3. [Audit coverage](discovery/audit-coverage.md) — inspection scope, findings and limits.
4. [Requirements register](requirements/requirements-register.md) — accepted direction and open questions.
5. [Import-review decision](design/decisions/001-import-review.md) — provisionally accepted behavior.
6. [Vault/platform boundaries](design/decisions/002-vault-platform-boundaries.md) — accepted direction with explicit open points.
7. [Knowledge navigation and review](design/decisions/003-knowledge-navigation-and-review.md) — agreed behavior, provisional preferences and unselected proposals.
8. [Workflow interpretation and execution](design/decisions/004-workflow-interpretation-and-execution.md) — agreed conceptual direction; naming and implementations open.
9. [Open questions](reviews/open-questions.md) — unresolved details and review gates.
10. [Historical alternatives](design/explorations/historical-alternatives.md) — options to reconsider.
11. [Evidence guide](discovery/evidence/README.md) — source index and recovery instructions.

## Authority and record types

- Requirements describe user needs and acceptance status, with verification links added when implemented.
- Inventory inclusion preserves an idea for evaluation, not a commitment to implement it.
- Explorations retain alternatives, trade-offs and unresolved questions.
- Decision records state status, context, rationale and consequences; supersede them explicitly.
- Old source text, including words such as final or locked, does not override current user instructions.
- Current explicit user direction governs. Document updates must not silently broaden approval.

## Working sequence

Complete extraction and obtain user confirmation -> brainstorm remaining requirements/questions ->
review a starting draft design -> obtain explicit authorization for a new implementation repository and IntelliJ setup.

## Maintenance

Discuss ideas in chat and retain substantive outcomes here. Update affected records and the checkpoint after each session.
Connect requirements, inventory IDs, decisions and later implementation/tests.
Record retain/refactor/merge/redesign/migrate/defer/remove dispositions with rationale and user review.

This is repository-level documentation, not a Java package.
Its location does not determine implementation organization. Decision 002 records the subsequently accepted separate platform/vault repository direction; detailed architecture remains open.

## Repository purpose and continuity

This private planning repository is separate from the future implementation repository and knowledge vault. Neither has been created by this migration. The long-term location of planning documents may be reconsidered explicitly later.

Start a new chat by supplying this repository URL and asking the assistant to read this README, the current checkpoint, requirements and decision records before continuing. A suggested resume message is in [RESUME.md](RESUME.md).

Record substantive outcomes with accepted/proposed/provisional/deferred/superseded status, rationale, evidence and open questions. Update the checkpoint, review the diff and publish authorized changes. Do not keep a second evolving copy in learning-assistant. Git only preserves changes that are committed; the remote only receives pushed changes.

See [migration provenance](reviews/planning-repository-migration.md) for source commits and preservation limits. Preserve the origin repository or migrate required source evidence before retiring it.

## Contribution workflow

Use a separate branch and pull request for ongoing changes, including documentation. Do not work directly on or push directly to main. Review/validate changes, publish the branch and PR, and merge only when authorized. Initial repository population and a subsequent direct push predated this user clarification; do not rewrite history to manufacture retroactive PRs. Branch protection has not been configured, so this is a workflow rule rather than a verified server-enforced restriction.

## Latest coverage review

[October 28 holistic review](reviews/2026-10-28-holistic-review.md) records verified baselines, corrections, remaining work and inspection limits. No review establishes exhaustive semantic coverage or approves an implementation architecture.

## Starting architecture draft

The user authorized drafting on 2026-10-31 using the inventory as a working baseline, without claiming exhaustive coverage or approving implementation. The [first workflow architecture draft](design/explorations/001-workflow-architecture-draft.md) tests shared responsibilities against revision, search/navigation and capture/enhancement. These examples do not limit platform scope. Review proposals iteratively before choosing modules, interfaces or a stack.

The [identity/versioning exploration](design/explorations/002-note-identity-and-versioning.md) develops portable note identity, navigation through moves and reviewed-change preconditions. These recommendations remain proposed, with metadata/link formats and concurrency mechanisms open.

The [information-model draft](design/explorations/004-note-information-model.md) distinguishes authored knowledge, inferred suggestions, derived views and review/session information. Review this next; whole-note metadata and concrete fields remain provisional proposals. [RESUME.md](RESUME.md) supplies a detailed copy-paste handoff with the current publication caveat.
