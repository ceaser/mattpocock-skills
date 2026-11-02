---
name: implement
description: "Implement a piece of work based on a spec or set of tickets."
disable-model-invocation: true
---

Implement the work described by the user in the spec or tickets.

The issue tracker should have been provided to you. If not, tell the user to run `/setup-matt-pocock-skills`.

If the user passes a ticket reference, fetch the relevant ticket the way the tracker doc says and state its title before starting. If the reference is ambiguous, ask. When the ticket cites a parent spec (an epic, a parent issue, a spec file), read the parent spec the way the tracker doc says: once, scoped to the sections the ticket cites, never the whole document.

Call the Skill tool with "tdd" where possible, at pre-agreed seams.

Run typechecking regularly, single test files regularly, and the full test suite once at the end.

Once done, call the Skill tool with "code-review" to review the work.

Commit your work to the current branch.
