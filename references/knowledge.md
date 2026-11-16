# Recording Project Knowledge

Read this guide when the user requests learning, recording, or updating project knowledge. Read the existing index and relevant entries before making incremental changes.

## Location and Index

Use `.team-context/` at the target project's root by default, or the location specified by the user. Create topic files only when there are findings to save; do not create empty topics.

| File | Contents |
| --- | --- |
| `index.md` | Project identity, source scope, topic paths and summaries, checked versions, and open questions |
| `project.md` | Architecture facts, entry points, business flows, terminology, and development and verification methods |
| `code-style.md` | Coding conventions and examples scoped by repository, module, or designated author |
| `document-style.md` | Structure, wording, level of detail, and examples scoped by document type |
| `reporting-style.md` | Reporting and presentation preferences and examples scoped by audience and occasion |

Keep `index.md` as a navigation aid rather than a duplicate of the topic files. On creation, record an identifiable repository or project, the authorized source scope, and relative paths to the topics actually created. Later, update only affected index entries.

Share knowledge across repositories only within a scope and mapping explicitly provided by the user. Identify the repository in code references. Do not automatically merge knowledge from unrelated parent directories, companies, or repositories, or infer company identity from a temporary directory name.

## Evidence-Backed Entries

Include the following information in each fact or rule. Equivalent wording in an existing format is sufficient; no machine-readable schema or numbering system is required.

| Field | Requirement |
| --- | --- |
| Content | A specific fact or actionable convention that changes a decision, rather than vague advice such as "write elegant code" |
| Scope | The relevant repository, module, language, document type, reference author, or audience |
| Evidence | Original paths or links with symbols, sections, or specific review comments; include a commit or document version and check date when available |
| Status | One of the evidence levels below, with the basis for the conclusion |
| Exceptions | Only exceptions or limits supported by evidence |

Use these statuses:

- **Confirmed**: Current guidance, an explicit user requirement, or a directly verified implementation fact. Distinguish requirements from observed behavior and record disagreements separately.
- **Supported by examples**: Several relevant, independent examples agree. This is an observed convention, not a mandatory policy.
- **Unconfirmed**: Insufficient examples, uncertain authorship, conflicting sources, or unverified freshness. Do not turn it into a mandatory rule that blocks work.
- **Obsolete**: Replaced by clearer evidence or confirmed to no longer apply. If retained, explain why and point to the replacement.

Ground entries in actual sources; do not save illustrative examples as company facts. Prefer references to original code. Quote short, necessary excerpts with attribution rather than copying entire repositories or documents.

## Verify the Evidence

- A merged change, file authorship, or lack of objections does not establish explicit acceptance of a detail. Mark something as accepted only when actual feedback or a user statement supports it.
- Do not invent versions, line numbers, dates, identities, or command results. Label unexecuted test and startup commands as "found in configuration; not yet verified."
- Check relevant entries against current configuration or comparable implementations. Inspect affected changes when a commit or file comparison is available; otherwise revisit relevant original sources instead of requiring a full rescan.
- Prefer source references and distilled findings. Omit credentials, customer data, and unrelated personal information. Process sources only with tools and services authorized by the user and permitted by the company.

## Update Existing Knowledge

Maintain a usable current conclusion. Reuse entries, add evidence, narrow the scope, or replace obsolete content. Do not duplicate the same rules or append entire conversations after every learning session.

Resolve conflicts by checking scope, freshness, and evidence. When a replacement is clear, update the conclusion and briefly record why. Otherwise mark it unconfirmed and preserve references to both sources. Keep differently scoped rules separate.

After writing, verify that index targets exist, references can be located, additions have evidence, and unrelated entries are unchanged. Briefly report the locations, substantive changes, and unresolved conflicts.

## Persistent Integration

Merge a short entry into existing project instructions only when the user requests this integration. For projects using `AGENTS.md`, instruct the agent to read `.team-context/index.md` for tasks involving team conventions, select topics for the current module, deliverable, and audience, and check relevant sources.

Preserve the structure and precedence of existing guidance. Use other tools' native entry points as appropriate. If automatic loading has not been verified, use explicit invocation rather than promising automatic activation.
