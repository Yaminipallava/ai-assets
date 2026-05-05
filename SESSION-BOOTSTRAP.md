# Session Bootstrap

Use this file to start an AI agentic session with a consistent loading order.

The goal is to combine:
- provider-specific behavior
- shared operational workflow
- project-specific overlays
- repo-local rules

## Load Order
Use this order unless a project explicitly overrides it:

1. provider overlay
2. shared core docs
3. project overlay
4. target repo local instructions such as `AGENTS.md`

Reason:
- provider docs explain how the agent behaves
- shared docs explain how work should be executed
- project docs explain what differs for a given product or organization
- repo-local files remain the last-mile source of truth

## Generic Core Files
Load these for most implementation sessions:

- `agents/operating-model.md`
- `agents/branch-hygiene.md`
- `workflows/story-intake.md`
- `workflows/implementation-flow.md`
- `workflows/pr-and-merge-flow.md`
- `workflows/post-merge-cleanup.md`

Load these when the task needs them:

- `agents/jira-gap-and-bug-handling.md`
- `workflows/sprint-review.md`
- `commands/jira-rest.md`
- `commands/confluence-rest.md`
- `commands/validation-commands.md`

## Provider Overlay
Add the provider-specific docs that match the active agent system.

Examples:

### Codex
- `providers/codex/README.md`
- `providers/codex/agent-instructions.md`
- `providers/codex/jira-confluence-usage.md`

### Claude
- `providers/claude/README.md`
- `providers/claude/agent-instructions.md`
- `providers/claude/jira-confluence-usage.md`

### Gemini
- `providers/gemini/README.md`
- `providers/gemini/agent-instructions.md`
- `providers/gemini/jira-confluence-usage.md`

### Oli
- `providers/oli/README.md`
- `providers/oli/provider-contract-notes.md`

Use `providers/oli/` only as a placeholder until a real provider contract exists.

## Project Overlay
After the provider and shared core are loaded, add the relevant project overlay.

Example:
- `projects/nunneri/README.md`
- `projects/nunneri/project-overview.md`
- `projects/nunneri/domain-rules.md`

Project overlays should only contain examples and conventions that differ from the shared core.

## Repo-Local Instructions
Finally, load repo-local instructions from the active code repository, for example:

- `AGENTS.md`
- repo-local contributor guidance
- repo-local architecture notes

Treat those as the final authority for that repo.

## Copy-Paste Session Prompt
Use this as a starting point and replace paths as needed:

```text
Use /home/pallava/Documents/suranku/repo/ai-assets as the shared operating guide.

Load in this order:
1. providers/<provider>/README.md
2. providers/<provider>/agent-instructions.md
3. agents/operating-model.md
4. agents/branch-hygiene.md
5. workflows/story-intake.md
6. workflows/implementation-flow.md
7. workflows/pr-and-merge-flow.md
8. workflows/post-merge-cleanup.md
9. projects/<project>/README.md
10. projects/<project>/project-overview.md
11. projects/<project>/domain-rules.md
12. the target repo local AGENTS.md

Follow repo-local instructions as final authority.
Use Jira and Confluence workflows from ai-assets only when they do not conflict with repo-local rules.
```

## Notes
- Do not put secrets in this repo.
- Keep machine-local env files outside repos.
- Keep provider-specific prompt syntax out of the shared core docs.
