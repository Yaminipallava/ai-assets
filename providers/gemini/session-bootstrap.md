# Gemini Session Bootstrap

Use this file when starting a Gemini-based agent session.

## Load Order
1. `providers/gemini/README.md`
2. `providers/gemini/agent-instructions.md`
3. `providers/gemini/jira-confluence-usage.md`
4. `agents/operating-model.md`
5. `agents/branch-hygiene.md`
6. `agents/jira-gap-and-bug-handling.md` when the task may reveal gaps
7. `workflows/story-intake.md`
8. `workflows/implementation-flow.md`
9. `workflows/pr-and-merge-flow.md`
10. `workflows/post-merge-cleanup.md`
11. project overlay docs
12. target repo local `AGENTS.md`

## When To Use
Use this when:
- taking a Jira story into implementation
- reviewing sprint delivery against acceptance criteria
- syncing repo behavior with Confluence
- preparing a PR with the expected branch and status workflow

## Gemini-Specific Notes
- provider-specific behavior belongs in the `providers/gemini/` folder
- generic workflow decisions should still come from the shared core docs
- repo-local `AGENTS.md` remains the final authority for the active repo
- if Jira or Confluence access depends on machine-local env files, keep those outside repos

## Recommended Nunneri Session
For Nunneri, also load:
- `projects/nunneri/README.md`
- `projects/nunneri/nunneri-agent-bootstrap.md`
- the target Nunneri repo local `AGENTS.md`

## Copy-Paste Prompt
```text
Use ai-assets as the shared operating guide.

For this Gemini session, load:
- providers/gemini/README.md
- providers/gemini/agent-instructions.md
- providers/gemini/jira-confluence-usage.md
- agents/operating-model.md
- agents/branch-hygiene.md
- workflows/story-intake.md
- workflows/implementation-flow.md
- workflows/pr-and-merge-flow.md
- workflows/post-merge-cleanup.md

If this is a Nunneri session, also load:
- projects/nunneri/README.md
- projects/nunneri/nunneri-agent-bootstrap.md
- the target repo local AGENTS.md

Follow repo-local instructions as final authority when they conflict with generic guidance.
```
