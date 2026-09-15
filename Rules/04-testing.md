# Testing Rules

Every meaningful code change should have appropriate validation.

## Testing Pyramid

Prefer:

1. Unit tests
2. Integration tests
3. API tests
4. End-to-end tests

Use E2E tests for critical user journeys rather than every small function.

## New Features

For new functionality:

- test happy path
- test validation failures
- test authorization
- test error conditions
- test important edge cases

## Bug Fixes

Every bug fix should ideally include a regression test.

The test should fail before the fix and pass after the fix.

## Do Not

Never modify tests merely to make the implementation pass.

First determine whether:

- implementation is wrong
- test expectation is wrong
- environment is wrong
- dependency behavior changed

## Validation

After modifications:

1. Run targeted tests.
2. Run related integration tests.
3. Run the full suite when practical.
4. Run build/lint/static analysis.
5. Review failures rather than ignoring them.