# Team Onboard

An agent skill that helps new developers understand an existing project and work in its team's style.

Team Onboard learns from authorized code, technical documents, and review feedback. It records evidence-backed guidance in the target project and retrieves only what the current task needs.

## What It Helps With

- Understand architecture, business flows, entry points, and where a change belongs.
- Learn a team's or a named developer's coding conventions from relevant examples.
- Match the structure and level of detail of company design documents.
- Adapt reports and presentations to a specific audience and occasion.
- Update project guidance from review comments and accepted changes.

The skill keeps facts, explicit requirements, observed conventions, and uncertain inferences distinct. It helps reduce avoidable review rework; it does not guarantee approval.

## Install

Using the [Skills CLI](https://skills.sh/docs):

```bash
npx skills add https://github.com/GX020124/team-onboard --skill team-onboard
```

Follow the installer prompts to choose your agent and installation scope.

For manual installation, copy this repository's contents into a skill directory supported by your agent. For a repository-scoped Codex installation, use `.agents/skills/team-onboard/`. See the [official Codex skill documentation](https://learn.chatgpt.com/docs/build-skills) for discovery and invocation details.

The skill itself requires no scripts, database, or API keys. Reading sources, editing code, and producing document or presentation files use the capabilities already available in your agent.

## Use

In Codex, invoke `$team-onboard` with a task and the project or materials to use:

```text
Use $team-onboard to walk me through this repository. Trace one real
business flow and explain which modules and tests I should read first.
```

```text
Use $team-onboard to learn the order module's conventions and Alex's
recent comparable changes. Save evidence-backed findings in this project.
```

```text
Use $team-onboard to implement this endpoint using the module's existing
conventions. Explain the relevant call chain and verify the change.
```

```text
Use $team-onboard to draft a design proposal using these accepted
documents as style references. Use the current requirement for facts.
```

```text
Use $team-onboard to prepare a presentation for the engineering lead.
Follow these accepted examples and use only the progress data provided.
```

```text
Use $team-onboard to update the relevant project guidance from these
review comments and the final accepted changes.
```

Ordinary questions and development tasks read existing knowledge without changing it. Requests to learn, record, or update project knowledge save findings within the authorized scope.

## How It Works

1. Identify the project, task, relevant module, deliverable, and audience.
2. Read the relevant workflow guide and project knowledge, then check the original sources that matter to the task.
3. Explain, implement, or write using applicable guidance and examples.
4. Verify the result and, when requested, update the affected knowledge entries.

Each saved entry includes its content, scope, evidence, status, and any supported exceptions. Personal preferences stay scoped to their context. Obsolete guidance is excluded from generation, and unconfirmed observations are not promoted to mandatory policy.

## Project Knowledge

Reusable instructions stay in this skill. Company-specific knowledge belongs in the target project, by default:

```text
.team-context/
  index.md
  project.md
  code-style.md
  document-style.md
  reporting-style.md
```

Only topics with actual findings are created. Existing knowledge locations can be used instead. A new session can reload the index when the skill is invoked; saving files alone does not guarantee automatic activation. Persistent integration with an existing `AGENTS.md` or another tool's guidance is available when requested.

Project knowledge may contain private company material. This repository ignores `.team-context/`; add that entry to the target project's `.gitignore` too when its knowledge should remain private. This repository's ignore rules do not automatically apply to other projects. Use only sources and processing tools authorized for the material.

## Repository Structure

```text
SKILL.md
agents/
  openai.yaml
references/
  onboarding.md
  code-style.md
  document-style.md
  reporting-style.md
  feedback.md
  knowledge.md
```

[SKILL.md](SKILL.md) selects workflows and defines shared rules. The [reference guides](references/knowledge.md) describe targeted procedures and the shared knowledge format. `agents/openai.yaml` provides Codex display metadata.

## Contributing

Keep changes focused, preserve evidence and authorization boundaries, and check internal links. Describe workflow changes with realistic examples, including how missing or conflicting evidence should be handled. Do not contribute private company sources or generated project knowledge.

Use English for repository content, code comments, commit messages, and pull requests.

## License

[MIT](LICENSE). Copyright (c) 2026 caiyanbin.
