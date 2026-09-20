---
"mattpocock-skills": patch
---

to-tickets: gate the parent spec behind the tickets it publishes. After publishing, the parent is made blocked by every ticket, using the tracker's native blocking edge (on GitHub, `gh issue create --parent <spec> --blocking <spec>`, or `gh issue edit <spec> --add-blocked-by <n>` after the fact) and a `Blocked by:` line in local mode. The parent keeps its `ready-for-agent` label, because it is still fully specified; what says "not yet" is the edge, not the label. This closes the most-reported rough edge on `to-spec`, where an AFK runner polling for `ready-for-agent` grabbed the parent spec and tried to build the whole feature in one run instead of working the ticket slices. `to-spec` now says what the label does and does not mean, and the `triage-labels.md` seed tells runners to grab from the frontier (blockers all closed) rather than from a raw label query.
