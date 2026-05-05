# Nunneri Agent Bootstrap

Use this file to start an agent session for the Nunneri repositories.

## Recommended Load Order
1. provider overlay from `providers/`
2. shared core workflow docs
3. Nunneri project overlay
4. Nunneri repo-local `AGENTS.md`

## Minimum Shared Core
Load these first:

- `agents/operating-model.md`
- `agents/branch-hygiene.md`
- `workflows/story-intake.md`
- `workflows/implementation-flow.md`
- `workflows/pr-and-merge-flow.md`
- `workflows/post-merge-cleanup.md`

Load these when needed:

- `agents/jira-gap-and-bug-handling.md`
- `workflows/sprint-review.md`
- `commands/jira-rest.md`
- `commands/confluence-rest.md`
- `commands/validation-commands.md`

## Nunneri Overlay
Load these next:

- `projects/nunneri/README.md`
- `projects/nunneri/project-overview.md`
- `projects/nunneri/jira-env-pattern.md`
- `projects/nunneri/domain-rules.md`
- `projects/nunneri/story-execution-example.md`
- `projects/nunneri/confluence-sync-example.md`

## Target Repo Local Files
For the main Nunneri product repo, also load:

- `/home/pallava/Documents/suranku/repo/Nunneri-Labs/nunneri/AGENTS.md`

When the task is architecture-heavy, also inspect:

- `/home/pallava/Documents/suranku/repo/Nunneri-Labs/nunneri/docs/architecture/`

## Nunneri-Specific Expectations
- branch names follow Jira keys such as `KAN-33`
- commit titles start with the Jira key
- PR titles start with the Jira key
- Jira status should move with real work progression
- merged local and remote branches should be cleaned up promptly
- missing implementation gaps should become tracked Jira items instead of undocumented follow-ups

## Jira and Confluence
Recommended local env pattern:

```bash
source ~/.config/nunneri/jira.env
```

Use the shared command/workflow docs for:
- reading and transitioning Jira issues
- creating Story, Bug, Spike, or Subtask follow-ups
- reading and updating Confluence architecture pages

## Copy-Paste Session Prompt
```text
Use /home/pallava/Documents/suranku/repo/ai-assets as the shared operating guide.

For this Nunneri session, load:
- providers/<provider>/README.md
- providers/<provider>/agent-instructions.md
- providers/<provider>/jira-confluence-usage.md
- agents/operating-model.md
- agents/branch-hygiene.md
- agents/jira-gap-and-bug-handling.md
- workflows/story-intake.md
- workflows/implementation-flow.md
- workflows/pr-and-merge-flow.md
- workflows/post-merge-cleanup.md
- projects/nunneri/README.md
- projects/nunneri/project-overview.md
- projects/nunneri/jira-env-pattern.md
- projects/nunneri/domain-rules.md
- /home/pallava/Documents/suranku/repo/Nunneri-Labs/nunneri/AGENTS.md

Follow the Nunneri repo local AGENTS.md as final authority when it conflicts with generic guidance.
```
