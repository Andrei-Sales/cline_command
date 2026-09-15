# Feature Development Workflow

Use this workflow when implementing a feature.

## Phase 1 — Understand

Inspect:

- repository structure
- relevant modules
- existing implementation patterns
- tests
- configuration
- dependencies

Identify affected areas.

## Phase 2 — Plan

Create a concise implementation plan:

1. Files to modify
2. Files to create
3. Data changes
4. API changes
5. Frontend changes
6. Tests
7. Deployment considerations

Do not implement yet if the requested change has significant architectural impact.

## Phase 3 — Implement

Implement incrementally.

After each meaningful change:

- inspect the result
- check compilation/type errors
- preserve existing behavior

## Phase 4 — Test

Run:

- targeted unit tests
- integration tests when relevant
- frontend tests when relevant
- build
- lint/static analysis

## Phase 5 — Review

Review the final diff for:

- correctness
- security
- unnecessary changes
- duplicated code
- error handling
- logging
- tests
- backwards compatibility

## Phase 6 — Report

Provide:

### Implemented
What changed.

### Files
Files modified/created.

### Tests
Commands executed and results.

### Risks
Known limitations.

### Next Steps
Only if necessary.