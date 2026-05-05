# Operating Model

Use this model across providers and projects unless a project overlay overrides it.

Core rules:
- start from a tracked work item
- review acceptance criteria before implementation
- inspect repo and docs before changing anything
- keep one active feature branch per work item by default
- validate locally before preparing a PR
- update Jira as work moves through real states

When to update Jira:
- `To Do` -> `In Progress` when implementation starts
- child items -> `Done` when their deliverable is actually complete
- parent item -> `In Review` when the branch is pushed and ready for PR review
- parent item -> `Done` only after merge is complete

Documentation expectations:
- update repo docs when implementation changes behavior or process
- update architecture docs when a design decision becomes implementation truth
- sync Confluence only when the project uses it and the repo change materially affects shared understanding
