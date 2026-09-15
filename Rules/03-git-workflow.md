# Git Workflow Rules

Use Git safely.

## Before Changes

Inspect:

- git status
- current branch
- recent commits
- existing modifications

Never overwrite unrelated uncommitted changes.

## Commits

Prefer small logical commits.

Commit messages should describe the change.

Examples:

feat: add user role management
fix: prevent duplicate student enrollment
refactor: extract authentication service
test: add validation tests for registration
docs: update deployment instructions

## Before Commit

Run relevant:

- tests
- build
- lint
- formatting
- static analysis

## Never

Do not:

- force push unless explicitly requested
- reset/delete user changes
- rewrite history unnecessarily
- commit secrets
- commit generated artifacts unless project convention requires them

## Pull Requests

A PR should explain:

- What changed
- Why it changed
- How it was tested
- Known limitations
- Migration requirements
- Deployment considerations