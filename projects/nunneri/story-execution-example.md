# Story Execution Example

Typical Nunneri flow:
1. read the Jira story and subtasks
2. inspect repo docs and current implementation state
3. create a branch named from the Jira key
4. implement the required change
5. run root validation commands
6. mark completed subtasks done
7. push branch and prepare PR
8. move the parent story to `In Review`
9. after merge, move it to `Done` and clean branches
