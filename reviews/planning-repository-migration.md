# Planning repository migration

Date: 2026-10-27. Status: completed authorized documentation migration.

The user authorized the proposed dedicated planning repository with "do what u think best" after the recommendation to transfer records, retain evidence links and leave a pointer in learning-assistant. Private visibility was selected to avoid publishing future personal planning by default; no implementation or vault repository creation was authorized.

## Provenance

Source: [learning-assistant planning directory at df7ef8a](https://github.com/saharshpoddarorg/learning-assistant/tree/df7ef8a30be8854e8e9ae139b80f8db1bcfc8802/docs/personal-digital-platform).
The directory was extracted with git subtree split. File contents were verified byte-for-byte before migration-specific edits. The three planning commits retain their authorship, messages and document history, with rewritten commit IDs because the paths became repository-root paths.

| Original commit | Extracted commit |
|---|---|
| a943f3b3485870267ed1dc5e4668e654ca37cc7c | 0b9dd7a |
| f992bced19c914ba4d168facba228f75f7a31e59 | 137bc04 |
| 73ed234536625582625491d40e6f2403732c516c | 4b35ce7 |

Original merge PRs: [91](https://github.com/saharshpoddarorg/learning-assistant/pull/91), [92](https://github.com/saharshpoddarorg/learning-assistant/pull/92), [93](https://github.com/saharshpoddarorg/learning-assistant/pull/93).

## Authority and limits

This repository is the single active home for planning records. The old planning directory was replaced with a relocation pointer in merged [PR 94](https://github.com/saharshpoddarorg/learning-assistant/pull/94), after this repository was published and verified; original documents remain recoverable at the pinned source commit.

The source index still points to learning-assistant, including historical blob hashes. Source code, raw extraction files, credentials and unrelated experimental material were not migrated. Recover original source blobs from the origin repository, not this filtered planning checkout. A metadata index is not a backup of source contents.

This migration changes documentation location, not accepted product scope or architecture. The final disposition of planning documents when implementation begins remains open.
