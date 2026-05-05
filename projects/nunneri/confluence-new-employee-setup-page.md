# Confluence Page: New Employee Setup for Nunneri Agentic Work

Use this page content in Confluence for employee onboarding.

## Summary
This guide helps a new employee prepare their system for Nunneri engineering work with AI agents. It covers repo setup, GitHub access, Jira and Confluence access, session bootstrap, and the expected branch and review workflow.

## What To Install
- Git
- SSH client
- the required language runtimes and package managers used by the target repo
- access to one supported AI provider:
  - Claude
  - Codex
  - Gemini
  - future `Oli`

## What To Clone
Create a local workspace folder of your choice and clone:
- `ai-assets`
- the target product repo such as `nunneri`

Keep these roles separate:
- `ai-assets` contains shared operational guidance
- the product repo contains product code and repo-local rules

## GitHub Access
1. Configure the correct GitHub identity for Nunneri work.
2. Add the SSH public key to the correct GitHub account.
3. Verify the repo remote uses the right SSH identity or alias.
4. Confirm the employee can fetch and push before starting work.

## Jira and Confluence Access
Create a machine-local env file outside all repos.

Recommended variable names:
- `JIRA_BASE_URL`
- `JIRA_EMAIL`
- `JIRA_API_TOKEN`
- `JIRA_PROJECT_KEY`

Rules:
- keep tokens out of repos
- do not store secrets in markdown files
- reuse the same Atlassian token for Jira and Confluence when appropriate

## Session Bootstrap
Start the session by loading:
1. the provider-specific overlay
2. the shared `ai-assets` operational docs
3. the Nunneri project overlay
4. the target repo local `AGENTS.md`

Recommended bootstrap docs:
- `SESSION-BOOTSTRAP.md`
- `projects/nunneri/nunneri-agent-bootstrap.md`

## Working Rules
- branch names follow the Jira key
- commit titles start with the Jira key
- PR titles start with the Jira key
- Jira status moves with actual work progress
- local validation runs before PR review
- merged branches are cleaned up locally and remotely
- any real gap becomes a tracked Story, Bug, or Spike

## Validation
Use the target repo’s root validation commands wherever possible:
- lint
- typecheck
- test

## First-Day Checklist
- clone the required repos
- verify GitHub SSH access
- create the Jira and Confluence env file
- read the shared and project bootstrap docs
- read the target repo local `AGENTS.md`
- confirm validation commands run
- start the first Jira-backed branch

## Related Internal Docs
- project bootstrap guide
- repo local `AGENTS.md`
- architecture overview
- sprint review workflow
