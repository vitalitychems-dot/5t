---
name: Tessera consolidation gate
description: Scope, source-retention, and completion rules for the Tessera multi-repository migration.
---

For this migration, Grok-ready is the final repository and TX is the staging repository. The owner’s rule is “include everything; remove only redundancy.” Account for distinct contributions and content; differences between versions are not duplicates by filename alone. Review excluded LFS archives, original images, vault data, and runtime records before calling the migration complete.

Do not publish secrets, personal records, private vault contents, or runtime/audit records to the public repositories. If any such material must be retained, account for it in an appropriate private destination without exposing its contents publicly. Keep every source repository and branch until all agents explicitly sign off against the same verified target commit. Then obtain the owner’s confirmation of the exact deletion list; do not delete anything before that.

**Why:** the owner clarified that prior omissions are not automatically approved as redundant and requires every agent’s explicit review before deciding on deletion.

**How to apply:** use this gate while comparing repositories, branches, archives, images, and private/runtime data; record paths, hashes, and dispositions in the shared review without posting sensitive contents.