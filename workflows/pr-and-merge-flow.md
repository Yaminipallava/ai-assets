# PR and Merge Flow

PR title pattern:
```text
<PROJECT>-123: short summary
```

PR body should capture:
- Jira item
- summary
- validation
- docs or ADR impact when relevant

Keep detailed work logs in:
- Jira comments
- PR body

Do not use commit messages as detailed work logs.

After merge:
- update Jira to `Done`
- sync local `main`
- delete the merged local branch
- verify remote branch cleanup
