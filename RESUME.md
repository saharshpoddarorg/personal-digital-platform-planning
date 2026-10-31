# Resume Personal Digital Platform architecture

Updated: 2026-10-31. Copy the block below into a new chat. The repository records carry the detailed capability/evidence history; this packet is a map, not a claim of exhaustive historical coverage.

```text
Resume my Personal Digital Platform architecture work as my senior architecture partner and pair-programming mentor. Work iteratively, challenge assumptions, explain trade-offs, and ask focused questions where needed. Do not turn tentative preferences into approved decisions.

AUTHORITATIVE RECORDS
Planning: https://github.com/saharshpoddarorg/personal-digital-platform-planning
Experimental reference: https://github.com/saharshpoddarorg/learning-assistant
Read current remote state, not cached chat history. Planning PRs #1–#4 were verified merged. PR #5 was open when this handoff was prepared and contains later agreements, the information-model draft and this handoff. Check its current status; if still open, read its branch codex/provisional-identity-tooling in addition to main. Do not assume a pushed PR is merged, or that merging a proposal approves the design.

Read:
- README.md, reviews/current-checkpoint.md, reviews/open-questions.md
- requirements/requirements-register.md (U01–U30)
- design/decisions/001-import-review.md through 004-workflow-interpretation-and-execution.md
- design/explorations/001-workflow-architecture-draft.md
- design/explorations/002-note-identity-and-versioning.md
- design/explorations/003-personal-project-tooling.md
- design/explorations/004-note-information-model.md
For coverage/history, consult discovery/source-inventory.md, discovery/audit-coverage.md, discovery/source-capability-crosswalk.md, discovery/candidate-detail-supplement.md, discovery/evidence/README.md, design/explorations/historical-alternatives.md, and reviews/2026-10-28-holistic-review.md. Trace original evidence through discovery/evidence/source-index.json. The inventory has 62 capability groups, bounded historical coverage, and undecided migration dispositions; do not restart the whole audit or claim exhaustive semantic coverage.

VISION AND BOUNDARIES
PKM and Learning first; Productivity/Planning and other domains remain future candidates. I will later create personal-digital-platform for a reviewed redesign. learning-assistant is evidence, not an architecture to copy. Separate platform and canonical Git-backed vault repositories are accepted direction; implementation/vault creation, scaffolding and IntelliJ configuration still require explicit authorization. A disposable local tool-evaluation sample exists but is not the actual vault; I decided the trial could be skipped. No installation or trial is a prerequisite.

KNOWLEDGE AND REVIEW
The vault must remain useful independently. Manual editors, deterministic code/APIs, configured flows and agents may participate. One canonical note can have multiple navigation routes. Authored knowledge and dynamic derived views are distinct; preserve understandable content and readable fallback without promising automatic fallback refresh.
Check related knowledge before integration; enhance existing notes instead of duplicating. Quick captures may stay inbox material; unresolved metadata must not hide content. Existing notes stay in place when edits need review. Mandatory/conditional/optional metadata is desired, but no schema or format is selected. Programming language is distinct from prose language. Hierarchical expandable navigation, relationships, search, authored learning paths and query-generated collections are desired; one primary parent is only provisional.
Proposed changes use independently meaningful checklist items grouped by note/section. Support iterative partial review, subset application by default as an offer, combined preview and dependency checks. Approval is proposal-version-specific; explicit authorization is required before application. Revisions affecting accepted portions need renewed review; already-applied changes are new amendments. Manual local edits are possible. Commit/push approval is separate from permission to edit/apply. Preserve conversion losses and conflicts for review. Storage, rollback and write concurrency remain open.
Stable note identity independent of path, exact reviewed versions, and pause/show differences if affected notes changed are PROVISIONAL defaults. I like pausing even for apparently unrelated edits but remain unsure; evaluate disruption before settling policy. ID format/storage and conflict-prevention mechanics are not approved.

WORKFLOWS AND TECHNOLOGY
Interpretation and execution are independently variable, connected by an explicit request. Non-AI, bounded-AI and agent-led modes are desired where useful; not three copies of every workflow. Visible defaults and explicit overrides, no silent AI escalation. Mode is not permission. Complete non-AI workflows are preferred where feasible; non-AI recap initially assembles authored material and discloses missing content. AI-generated output is not automatically accepted knowledge.
Java familiarity matters for maintainability, but Java/Gradle, API transports, agent integrations and module structure remain open. An in-process Java interface is not automatically an external API. Named AI assistants are examples, not verified interchangeable runtimes.
Revision is one example, alongside search/navigation and capture/enhancement. Guided revision provisionally offers up to three questions one at a time, skippable; answers tailor the session independently of saving progress. Immediate feedback and quick-recap/quiz/test variants remain proposals. Session tailoring does not settle chat/log retention.

TOOLING AND ACCESS
Mostly me, agents acting on my behalf and occasional friends. I want epic/story/task breakdown and an ideas backlog. Provisional direction: GitHub Free for development/backlog; Obsidian Free is the leading vault candidate, not a finalized choice. Jira/Confluence remain alternatives; pay only for concrete value. Desired page features include hierarchy, indexes/TOC, child/related listings, code, tables and issue links. Live issue reports are not established requirements. Do not equate folders with Confluence page hierarchy or promise all dynamic views work outside Obsidian.
Notion/Confluence editing remains desired early but not initially required; integration/fidelity is unverified. Phone priorities: read/search, refresh stale remote information and quick capture first; approval, finalized-note edits and commit/push lower. Offline and sync details remain open.

WHERE TO CONTINUE
We are ALREADY doing conceptual architecture design. The latest draft models whole-note information first, separating authored content/relationships, observed versions, derived views, capture/proposal state and session state. Examples: Java memory model, language-independent Strategy pattern with language-specific examples, and an Interview preparation path linking existing notes. Whole-note-first, minimal fields and derived reverse relationships are proposals, not an approved schema.
First summarize the actual checkpoint and publication status. Then review design/explorations/004-note-information-model.md with me. Next compare folder-derived navigation versus explicit parent relationships and determine the smallest useful metadata set. After semantics are clear, move toward concrete operation contracts and format/module trade-offs. Do not begin implementation. All O01–O17 remain visible; unresolved details are not a reason to repeat every earlier question.

CONTINUITY
Keep substantive outcomes in planning documents with proposed/provisional/accepted/deferred/superseded statuses, rationale and traceability. Use branches and PRs, never direct main pushes; merge only when authorized. Check current instructions and local changes before editing. Do not assume the private repository is already cloned or accessible. Report any access limitation rather than inventing the contents. No automatic background work is scheduled.
```

## Publication note

Check [PR #5](https://github.com/saharshpoddarorg/personal-digital-platform-planning/pull/5) for these updates before relying only on main. All future assistants should recheck live status. No handoff can guarantee retention of every historical sentence; the indexed evidence and explicit inspection limits preserve the basis for targeted follow-up.
