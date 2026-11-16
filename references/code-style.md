# Learning and Applying Coding Conventions

## Select Evidence

Read applicable project instructions, formatting and static-analysis configuration, and existing knowledge for the target module. Select a small set of recent, maintained implementations and tests matching the language, module, and change type. Expand the sample only to resolve specific uncertainty.

When the user names a reference author, narrow the sample using actual commits and changed sections, then inspect surrounding code and later changes. Author metadata and blame are only clues: merge commits, mechanical moves, and formatting can obscure attribution. Do not attribute an entire file's conventions to one person.

Prefer relevant examples with explicit review feedback. Generated code, dependency copies, bulk migrations, and mechanical formatting are usually poor evidence of personal preferences. When old and new patterns coexist, investigate scope and evolution instead of deciding by frequency alone.

## What to Learn

Extract conventions that affect development decisions and retain references to examples:

| Area | What to Observe |
| --- | --- |
| Files and naming | File boundaries, declaration and import order, naming, and exports |
| Layers and reuse | Placement of business logic, shared helpers, dependencies, and abstraction level |
| Data and control flow | Data structures, state representation, asynchronous work, branches, and returns |
| Errors and boundaries | Input validation, permission entry points, error propagation, logging, and response conventions |
| Tests | Test locations, doubles and fixtures, assertion priorities, and project checks |

Save only evidence-backed conclusions useful to later tasks. Absence of a pattern does not establish a prohibition. A short implementation or use of a particular pattern does not by itself establish the author's general philosophy.

When asked to learn or record conventions, follow the [knowledge guide](knowledge.md) and write to the target project's code topic, defaulting to `.team-context/code-style.md`. Use sections for modules and reference authors, with applicable examples and exceptions.

## Apply to Development

1. Read relevant knowledge and examples, then check current source and deterministic configuration. Without saved rules, consult comparable implementations directly and state the limits of the observations.
2. Find callers of the affected function or interface, plus related tests, configuration, and exports, to establish the complete change scope.
3. Preserve existing file organization, layers, and helpers. Apply conventions to the code required by this task, keep changes tied to the requirement, and remove unused material introduced by the change.
4. Verify behavior with appropriate checks. For bug fixes, prefer a focused check that reproduces the defect. Use sufficient existing checks for small changes; do not add tests merely to enforce prose or cosmetic preferences.

Explain concrete conflicts between a reference author's habits and the module's current requirements. Keep local choices local; resolve conflicts before changing interfaces or project conventions. Do not imitate defects, missing validation, or obsolete interfaces.

## Delivery Checks

- Confirm that behavior meets the requirement, affected call paths still work, and conventions match the target module.
- Report executed checks, results, and environment blockers accurately. Style similarity does not establish correctness or review approval.
- Ordinary implementation work does not update long-term knowledge. Make evidence-backed incremental updates when the user requests them.
