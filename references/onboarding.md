# Project Onboarding and Implementation Questions

Build a project map around what the newcomer needs to understand. Start broadly for general onboarding; start with the relevant call chain for a specific question and expand as needed.

## Investigation

1. Read applicable project instructions, documentation, dependencies, runtime configuration, tests, and CI configuration. Identify the business purpose, technology stack, main modules, and documentation entry points.
2. Search directories and symbols to locate entry points, module boundaries, interfaces, and data models. Skip dependency copies, build artifacts, and generated files. Check documentation claims against representative source code.
3. Trace one real flow relevant to the task through its entry point, validation and permissions, business logic, data access, and response. Use appropriate entry points for event consumers, background jobs, and command-line applications instead of forcing a request-response model.
4. Find development, test, and check commands in actual configuration. Keep discovery primarily read-only. Distinguish commands merely found from commands successfully executed, and respect the task's authorization and environment requirements when running checks.

Do not infer the whole architecture from framework or directory names alone. When external services, database definitions, or private documents are unavailable, state what can be established and which sources are missing.

## Onboarding Output

Select the content needed for the question rather than always producing a long report:

- The project's purpose and business concepts relevant to the task.
- Responsibilities and interactions of key modules, with a small diagram when useful.
- One business flow with actual files and symbols for each step.
- Where common changes belong and which comparable implementations and tests to consult.
- Discovered run and verification entry points, plus unverified details.

Give the newcomer enough navigation to proceed, then go deeper as requested. For a question about a function, explain that function and its necessary context directly.

## Answer Development Questions

When explaining where to make a change, identify entry points, shared logic, callers, and relevant tests. When explaining why an approach exists, distinguish behavior proven by code, documented design rationale, and inference. Do not invent historical decisions.

Identify the actual callers, interfaces, configuration, and tests a change may affect. For implementation work, read the [code style guide](code-style.md) and follow the real call chain through the required changes.

Keep an explanation within the question's scope; continue through implementation when the user requests it. Group questions requiring a team decision while continuing investigation that does not depend on them.

## Save and Verify

When asked to save onboarding findings, follow the [knowledge guide](knowledge.md), write reusable facts to the target project's project topic, defaulting to `.team-context/project.md`, and update the index. Answer ordinary questions without automatically saving knowledge.

Before delivery, check that key conclusions trace to code or documents, command results are represented accurately, and architecture facts remain distinct from recommendations.
