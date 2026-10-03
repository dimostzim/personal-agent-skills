---
name: implement
description: "Implement a piece of work based on a spec or set of tickets."
disable-model-invocation: true
---

Implement the work described by the user in the spec or tickets.

Apply the `coding` skill. Before editing, record the starting commit and existing worktree changes for review.

Use /tdd where possible, at pre-agreed seams.

Run typechecking regularly, single test files regularly, and the full test suite once at the end.

Once done, use /code-review with the recorded starting commit, the spec, and the final working tree including relevant untracked files. Address substantiated findings and verify the fixes using `coding`.
