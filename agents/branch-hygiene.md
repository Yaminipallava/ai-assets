# Branch Hygiene

Keep local and remote branches current.

Routine:
1. fetch with prune
2. confirm which work-item branches are already merged
3. delete stale local merged branches
4. verify remote branches were auto-deleted after merge
5. remove obsolete remote branches when auto-delete did not happen

Rules:
- do not keep long-dead feature branches around
- do not delete an unmerged branch that still contains unique work
- prefer clean `main` plus active feature branches only

Recommended checks:
- local branch list versus merged history
- remote branch list versus merged PRs
- Jira status versus actual branch/merge state
