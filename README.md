# ai-assets

Shared operational assets for AI agents working across repositories, providers, and projects.

This repo is intentionally:
- provider-neutral at the core
- markdown-first in v1
- reusable across projects

Start here:
- `SESSION-BOOTSTRAP.md`: how to compose provider, shared-core, project, and repo-local instructions for a live agent session
- `providers/codex/session-bootstrap.md`: direct Codex session startup guide
- `agents/`: operating rules for agents
- `commands/`: reusable command patterns
- `workflows/`: end-to-end execution playbooks
- `templates/`: PR, review, and audit templates
- `providers/`: provider-specific overlays
- `projects/`: project-specific examples and conventions

Getting started for Nunneri:
1. read `SESSION-BOOTSTRAP.md`
2. read `providers/codex/session-bootstrap.md` if using Codex
3. read `projects/nunneri/nunneri-agent-bootstrap.md`
4. read the target repo local `AGENTS.md`

Design rules:
- generic core docs must avoid provider-specific tool syntax
- provider folders may describe provider-specific auth, prompting, and execution patterns
- project folders should contain overlays and examples, not duplicated generic rules
- do not commit secrets, tokens, or machine-local values except as clearly marked examples
