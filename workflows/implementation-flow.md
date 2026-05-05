# Implementation Flow

Default execution sequence:
1. sync `main`
2. create a branch from the work-item key
3. move the story to `In Progress`
4. implement the smallest coherent slice
5. validate with repo commands
6. update completed subtasks
7. prepare docs if behavior changed
8. push branch
9. move parent story to `In Review`
10. prepare PR title and body

Rules:
- keep one work item per branch
- keep commit titles short and keyed
- do not treat a story as done until merge is complete
