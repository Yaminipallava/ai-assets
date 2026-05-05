# ai-assets

Shared operational assets for AI agents working across repositories, providers, and projects.

This repo is intentionally:
- provider-neutral at the core
- markdown-first in v1
- reusable across projects

Start here:
- `agents/`: operating rules for agents
- `commands/`: reusable command patterns
- `workflows/`: end-to-end execution playbooks
- `templates/`: PR, review, and audit templates
- `providers/`: provider-specific overlays
- `projects/`: project-specific examples and conventions

Design rules:
- generic core docs must avoid provider-specific tool syntax
- provider folders may describe provider-specific auth, prompting, and execution patterns
- project folders should contain overlays and examples, not duplicated generic rules
- do not commit secrets, tokens, or machine-local values except as clearly marked examples
