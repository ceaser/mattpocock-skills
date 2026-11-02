---
"mattpocock-skills": patch
---

`implement` now fetches a ticket and reads its parent spec the way the repo's `docs/agents/issue-tracker.md` says, instead of choosing the command itself. The tracker templates `setup-matt-pocock-skills` ships gain a `When a skill says "read the parent spec"` entry that reads the parent once, scoped to the sections the ticket cites, using machine-readable output so tables are not wrapped or truncated; hand-written "other" tracker docs are asked to carry the same headings. Re-run `/setup-matt-pocock-skills` to refresh a shipped template, or add the entry to a hand-written doc.
