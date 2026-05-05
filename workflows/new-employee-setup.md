# New Employee Setup

Use this guide for any new employee who needs to start AI-assisted engineering work across repos.

## Goals
- prepare a machine for Git-based engineering work
- configure access to GitHub, Jira, and Confluence
- clone the shared operational assets repo and the target product repo
- start an agent session with the correct bootstrap order

## Prerequisites
- Git
- SSH client
- required language runtimes and package managers for the target repo
- access to the relevant GitHub repositories
- access to the relevant Jira project and Confluence space
- access to one supported provider such as Claude, Codex, or Gemini

## Workspace Setup
Choose a stable local workspace root, for example:
- `~/workspace`
- `~/repos`
- `~/work`

Inside that workspace, clone:
- `ai-assets`
- the target product repo

Keep this separation:
- `ai-assets` contains shared operational guidance
- product repos contain code and repo-local rules

## GitHub Setup
1. configure the correct GitHub identity for the target org or repo
2. add the SSH public key to that GitHub account
3. verify the target repo uses the correct SSH identity or alias
4. confirm fetch and push access before starting work

## Jira and Confluence Setup
Create a machine-local env file outside repos.

Recommended variable names:
- `JIRA_BASE_URL`
- `JIRA_EMAIL`
- `JIRA_API_TOKEN`
- optional `JIRA_PROJECT_KEY`

Rules:
- do not commit the env file
- do not store tokens in markdown docs
- reuse the same Atlassian token for Jira and Confluence when appropriate

## Session Startup
Load in this order:
1. provider overlay
2. shared core docs
3. project overlay
4. target repo local `AGENTS.md`

Recommended shared core:
- `SESSION-BOOTSTRAP.md`
- `agents/operating-model.md`
- `agents/branch-hygiene.md`
- `workflows/story-intake.md`
- `workflows/implementation-flow.md`
- `workflows/pr-and-merge-flow.md`

## Working Rules
- branch names should follow the work item key
- commit titles should start with the work item key
- PR titles should start with the work item key
- update Jira status with real progress
- validate locally before PR review
- clean merged branches locally and remotely
- create Story, Bug, or Spike follow-ups for real gaps

## First-Day Checklist
- clone `ai-assets`
- clone the target repo
- verify GitHub SSH access
- create the Jira and Confluence env file
- read the provider bootstrap
- read `SESSION-BOOTSTRAP.md`
- read the project bootstrap
- read the repo-local `AGENTS.md`
- verify validation commands run
- start the first tracked branch
