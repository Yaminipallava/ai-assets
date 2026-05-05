# Confluence REST

Confluence can usually reuse the same Atlassian env values used for Jira:
- `JIRA_BASE_URL`
- `JIRA_EMAIL`
- `JIRA_API_TOKEN`

Typical operations:
- search pages by title or text
- read existing page storage content
- create a page under a known parent
- update a page version with new content

Use this when:
- architecture pages need to reflect implementation truth
- PRs change shared workflow, identity, routing, or product behavior

Keep Confluence updates:
- scoped
- non-duplicative
- linked to relevant Jira stories and ADRs where applicable
