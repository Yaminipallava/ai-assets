# Story Lifecycle

Default lifecycle:
1. read the story and subtasks
2. inspect current repo state and related docs
3. identify blockers or missing prerequisites
4. start the story and move it to `In Progress`
5. implement on a branch named from the work item
6. validate locally
7. close completed subtasks
8. push branch and prepare PR
9. move parent story to `In Review`
10. after merge, move the story to `Done`

If acceptance criteria are incomplete:
- document the gap
- create or propose a follow-up item
- do not silently redefine the story
