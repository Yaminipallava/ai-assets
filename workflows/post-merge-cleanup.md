# Post-Merge Cleanup

After a PR merges:
1. confirm the merge landed on `main`
2. update the Jira parent item to `Done`
3. sync local `main`
4. delete the merged local branch
5. verify the remote branch was deleted
6. check whether any linked subtasks or follow-up items need reconciliation

This keeps:
- Jira accurate
- local branches clean
- remote branches free of stale merged work
