---
name: coding
description: Apply the user's engineering standards when writing, modifying, debugging, refactoring, reviewing, or validating code.
---

# Coding

Apply these standards proportionally to the task and its risk. For routine edits and back-and-forth coding, work directly on the requested change and run appropriate checks; no spec, tickets, or full pipeline is required. `implement` coordinates the chosen spec-driven workflow, and `tdd` supplies a test-first method when selected.

## Understand the change

- Read project instructions, inspect the worktree, and define success as observable behavior. Reproduce the reported failing scenario when practical.
- Start with the narrow path needed for the requested behavior. Trace callers, consumers, and tests when the change can affect them; widen investigation only for a concrete dependency, uncertainty, or failure.
- Put behavior where its invariant belongs. Reuse canonical definitions and existing interfaces rather than duplicating business rules in wrappers. Verify consequential external facts from authoritative sources.

## Implement the smallest coherent solution

- Follow the project's naming, formatting, error-handling, and architectural conventions. Use explicit data flow and intention-revealing names.
- Preserve defaults, public interfaces, data formats, and failure behavior unless the task changes them. Add no speculative features, abstractions, dependencies, fallback paths, or compatibility layers.
- Prefer a local change in the existing structure. Add a helper, abstraction, configuration option, or fallback only when a concrete requirement or observed failure needs it. Small duplication is acceptable when extraction would add complexity without clarifying the current task.
- Validate at the relevant input or invariant boundary; do not manufacture plausible values for invalid state. Catch expected errors only where useful recovery exists. Account for partial, repeated, interrupted, and cleanup paths when the change involves stateful operations.
- Keep changes within scope. Preserve pre-existing tracked and untracked work; avoid unrelated refactoring, regeneration, and formatting. Remove only what your change makes obsolete. If a small fix starts becoming a refactor, reconsider the local solution and explain the concrete reason for the growth. Ask before expanding the requested scope.

## Verify and finish

- Use the smallest set of existing checks that meaningfully covers the changed behavior. Add focused tests for substantial new behavior or meaningful regressions; routine edits do not need new test infrastructure or an exhaustive edge-case suite.
- Before adding a lasting test, identify the behavior or real regression it protects and the coverage existing tests lack. Prefer extending an existing test; avoid duplicate tests, tests of trivial implementation details, and fixtures or helpers without a lasting purpose.
- Exercise the actual entrypoint or boundary when a change crosses one. Test observable behavior with independently justified expectations, rather than internal structure, source-text matching, or incidental logs.
- Reuse the project's test infrastructure. Never weaken checks, skip relevant failures, or add broad fallbacks to manufacture a passing result.
- Put one-off harnesses, debug scripts, logs, and intermediate reports in the OS temporary directory or an established ignored scratch location. Use the repository only when the check requires it, and keep track of the temporary files and wiring you introduce.
- Before finishing, remove task-created temporary files, debug instrumentation, prototype routes, and incidental configuration. Preserve requested deliverables and useful regression tests. Remove redundant task-created experiments after a test covers the real failure; never delete pre-existing work or tests merely as cleanup. If something must remain for ongoing review, state its location and purpose.
- Inspect the complete final change, including untracked files, for unrelated edits, stale consumers, credentials, and temporary artifacts. Check the result against the request and fix substantiated in-scope defects.
- Stop when the requested behavior is implemented, appropriate checks pass, and the final change has been inspected. Broaden or repeat verification only for a new change, failure, or concrete unresolved concern. Leave optional cleanup and hypothetical improvements for a separate request.
- Report the outcome, verification performed, and material limitations. Distinguish checks that passed, failed, and were not run.
