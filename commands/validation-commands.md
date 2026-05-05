# Validation Commands

Validation should use the repo’s existing root command contract whenever possible.

Preferred pattern:
- `lint`
- `typecheck`
- `test`

Guidelines:
- prefer one stable root command per validation category
- do not duplicate command logic across PR docs, agent notes, and CI
- CI should call the same repo contract that humans and agents use locally

If a repo has split stacks:
- keep backend and frontend validation explicit
- still route them through one documented root interface where possible
