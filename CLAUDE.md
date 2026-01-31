# CLAUDE.md

There are a set of steering files I expect every repo to have. This includes:
- STEERING.md: A guide to agents that describe, in general, the workflow the agent should take when exploring and working on the codebase
- REPOSITORY.md: A high-level summary of the repository you are working in, including architecture, key API information, and any other useful information that a new engineer or agent would need when onboarding to the repo
- BUILDING.md: A description of how to build the library and run tests, if tests exist.
- HANDOFF.md: A file containing relevant context to preserve between sessions
- WORKLOG.md: A file containing *very concise* summaries of the work you did this session

Other than HANDOFF.md, if these files do not already exist, add them to .claude as your first step. Below is a set of baseline content for those files:

## STEERING.md:
### Communication
In all interactions and commit messages, be extremely concise and sacrifice grammar for the sake of concision
### GitHub
Use GitHub CLI if interacting with GitHub
### Git
If creating branches, prefix them with "feature/" where feature is the task being worked on
### Code Comments
Limit the use of superfluous code comments. All functions (other than boilerplate like main) should have a docstring explaining what the function *does*, and its inputs/outputs. Comments in the code bodies should be limited for snippits that are exceptionally hard to read. Favor clear naming and breaking things into smaller functions over commenting on every section of code you write.
### Code Review for Agent Work
When you feel the code is ready, submit a pull request for me to review and merge to main/mainline/master myself. You should **NEVER** push or force push to main/mainline/master.
### Clarification
If you feel like more information is needed or there are gaps in the task description, or you need input from the user on a design decision or execution task, ask the user before proceeding with your work.
### Test-Driven Development
If the code already has tests (or you are asked to add tests), you should follow test-driven development. This means:
- Start by writing tests that cover the feature set of the task you're implementing. These should fail as nothing is implemented.
- Begin implementation
- Iterate by running tests as you build
- Continue once the tests you've implented pass. This must be done faithfully, no returning "TRUE" or equivalent to force the tests to pass. 
- If you feel there is not enough information in the request to generate a broad set of tests, ask for more information from the user
- Aim for 90% code coverage, focusing on the happy path as well as failure cases
### Linting
If the code doesn't already have a linter setup, ask the user to set one up. If one exists (or for Python, if black is installed) keep all code up to the standard of the linter.
### HANDOFF.md
If you are running out of context, or are working on a multiphase task, add any information necessary for a completely fresh agent to pick up your work inside HANDOFF.md.
### WORKLOG.md
As you work, keep the worklog up to date. Keep it very concise. Should just be bullet points and date/time you did each task


