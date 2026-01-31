# STEERING.md

## Communication
In all interactions and commit messages, be extremely concise and sacrifice grammar for the sake of concision

## GitHub
Use GitHub CLI if interacting with GitHub

## Git
If creating branches, prefix them with "feature/" where feature is the task being worked on

## Code Comments
Limit the use of superfluous code comments. All functions (other than boilerplate like main) should have a docstring explaining what the function *does*, and its inputs/outputs. Comments in the code bodies should be limited for snippits that are exceptionally hard to read. Favor clear naming and breaking things into smaller functions over commenting on every section of code you write.

## Code Review for Agent Work
When you feel the code is ready, submit a pull request for me to review and merge to main/mainline/master myself. You should **NEVER** push or force push to main/mainline/master.

## Clarification
If you feel like more information is needed or there are gaps in the task description, or you need input from the user on a design decision or execution task, ask the user before proceeding with your work.

## Test-Driven Development
If the code already has tests (or you are asked to add tests), you should follow test-driven development. This means:
- Start by writing tests that cover the feature set of the task you're implementing. These should fail as nothing is implemented.
- Begin implementation
- Iterate by running tests as you build
- Continue once the tests you've implented pass. This must be done faithfully, no returning "TRUE" or equivalent to force the tests to pass.
- If you feel there is not enough information in the request to generate a broad set of tests, ask for more information from the user
- Aim for 90% code coverage, focusing on the happy path as well as failure cases

## Linting
If the code doesn't already have a linter setup, ask the user to set one up. If one exists (or for Python, if black is installed) keep all code up to the standard of the linter.

## HANDOFF.md
If you are running out of context, or are working on a multiphase task, add any information necessary for a completely fresh agent to pick up your work inside HANDOFF.md.

## WORKLOG.md
As you work, keep the worklog up to date. Keep it very concise. Should just be bullet points and date/time you did each task
