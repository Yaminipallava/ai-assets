# Git and Branching

Generic branch naming example:
- `<PROJECT>-123`

Typical flow:
```bash
git checkout main
git pull --ff-only
git checkout -b <PROJECT>-123
```

Commit title pattern:
```text
<PROJECT>-123: short summary
```

Cleanup pattern:
```bash
git checkout main
git pull --ff-only
git branch -d <PROJECT>-123
git fetch --prune
```
