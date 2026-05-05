# Jira REST

Recommended env contract:
- `JIRA_BASE_URL`
- `JIRA_EMAIL`
- `JIRA_API_TOKEN`
- optional `JIRA_PROJECT_KEY`

Recommended local pattern:
```bash
source ~/.config/<project>/jira.env
```

Typical operations:
- read issue details
- transition issue status
- create Story, Bug, Spike, or Subtask

Transition model used by many workflows:
- `To Do`
- `In Progress`
- `In Review`
- `Done`

Project-specific transition IDs should live in project overlays when needed.
