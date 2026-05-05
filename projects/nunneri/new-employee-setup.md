# New Employee Setup

Use this guide to prepare a new machine for Nunneri agentic work without relying on any one person's local file layout.

## Goals
- clone the required repos into a local workspace
- configure Git and GitHub access
- configure Jira and Confluence access through an env file
- load the shared `ai-assets` operating guides into an agent session
- start work on a Jira-backed branch with the expected validation and cleanup flow

## Prerequisites
- Git installed
- SSH client installed
- access to the Nunneri GitHub repositories
- access to the Nunneri Jira project and Confluence space
- one supported AI provider available for the session:
  - Claude
  - Codex
  - Gemini
  - future `Oli`

## Recommended Local Workspace
Choose a stable local workspace root such as:

- `~/workspace`
- `~/repos`
- `~/work`

Inside that workspace, clone the repos you need, for example:

- `ai-assets`
- `nunneri`

Keep this rule:
- shared operational assets live in `ai-assets`
- product code lives in the product repo

## GitHub Setup
1. Create or reuse the correct GitHub identity for Nunneri work.
2. Add the matching SSH public key to the GitHub account.
3. Configure the Git remote to use the correct SSH identity or alias for the Nunneri repos.
4. Verify push access before starting work.

Recommended checks:
- confirm `git remote -v`
- confirm the Git identity for the repo
- confirm a non-destructive GitHub operation works

## Jira and Confluence Setup
Create a machine-local env file outside all repos.

Recommended location pattern:

```bash
~/.config/nunneri/jira.env
```

Recommended variables:

```bash
export JIRA_BASE_URL="https://<your-org>.atlassian.net"
export JIRA_EMAIL="<your-email>"
export JIRA_API_TOKEN="<your-api-token>"
export JIRA_PROJECT_KEY="<project-key>"
```

Rules:
- do not commit the env file
- do not store tokens in repo files
- use the same env file for Jira and Confluence REST when both are hosted in the same Atlassian site

## Repos to Clone
At minimum:
- `ai-assets`
- the target product repo such as `nunneri`

Optional:
- any related example or legacy repos needed for behavior reference

## Session Bootstrap
Start the agent session by loading:

1. provider overlay from `ai-assets/providers/`
2. shared core docs from `ai-assets/agents/`, `commands/`, and `workflows/`
3. the Nunneri project overlay from `ai-assets/projects/nunneri/`
4. the target repo local `AGENTS.md`

Recommended starting docs:
- `SESSION-BOOTSTRAP.md`
- `projects/nunneri/nunneri-agent-bootstrap.md`

## Working Model
- branch names should follow the Jira key
- commit titles should start with the Jira key
- PR titles should start with the Jira key
- update Jira status with real work progress
- validate locally before opening a PR
- clean local and remote branches after merge
- create follow-up Story, Bug, or Spike items for real gaps instead of leaving them undocumented

## Validation Expectations
Use the target repo’s root validation commands where available:
- `lint`
- `typecheck`
- `test`

Do not invent alternate validation flows if the repo already defines them.

## First-Day Checklist
- clone `ai-assets`
- clone the target product repo
- verify GitHub SSH access
- create the Jira/Confluence env file
- read the shared bootstrap guide
- read the project bootstrap guide
- read the target repo local `AGENTS.md`
- verify repo validation commands run
- start the first Jira-backed branch
