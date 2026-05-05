# Oli Session Bootstrap

Use this file as the future session entrypoint when `Oli` becomes a real provider.

Current state:
- placeholder only
- not backed by a real provider contract yet
- no executable auth or API flow is defined here

## Planned Load Order
When the provider exists, the intended load order is:

1. `providers/oli/README.md`
2. `providers/oli/provider-contract-notes.md`
3. future `providers/oli/agent-instructions.md`
4. future `providers/oli/jira-confluence-usage.md`
5. shared core docs from `agents/`, `commands/`, and `workflows/`
6. project overlay docs
7. target repo local `AGENTS.md`

## What This File Reserves
This file reserves a stable place for:
- API-token auth notes
- provider capability notes
- provider-specific prompt and command overlays
- provider-specific session startup guidance

## Current Rule
Until the real provider exists:
- use the shared core and another active provider overlay
- do not add speculative wire formats or fake auth flows here
