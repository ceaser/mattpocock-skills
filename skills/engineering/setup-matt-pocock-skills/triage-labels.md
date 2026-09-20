# Triage Labels

The skills speak in terms of five canonical triage roles. This file maps those roles to the actual label strings used in this repo's issue tracker.

| Label in mattpocock/skills | Label in our tracker | Meaning                                  |
| -------------------------- | -------------------- | ---------------------------------------- |
| `needs-triage`             | `needs-triage`       | Maintainer needs to evaluate this issue  |
| `needs-info`               | `needs-info`         | Waiting on reporter for more information |
| `ready-for-agent`          | `ready-for-agent`    | Fully specified, ready for an AFK agent  |
| `ready-for-human`          | `ready-for-human`    | Requires human implementation            |
| `wontfix`                  | `wontfix`            | Will not be actioned                     |

When a skill mentions a role (e.g. "apply the AFK-ready triage label"), use the corresponding label string from this table.

`ready-for-agent` is a readiness state, not a queue. It says the issue is fully specified, not that it is workable right now: a parent spec keeps the label while `to-tickets` holds it blocked behind its tickets, unless the tracker refuses that edge, in which case the label comes off for the duration instead. Which applies is recorded in `issue-tracker.md`. An AFK runner should therefore grab from the **frontier** (issues carrying the label whose blockers are all closed) rather than from a raw label query, or it will pick up a spec and try to build the whole thing in one run.

Edit the right-hand column to match whatever vocabulary you actually use.
