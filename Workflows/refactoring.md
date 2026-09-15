# Refactoring Workflow

The primary requirement is preserving behavior.

## Before

Identify:

- current behavior
- callers
- dependencies
- tests
- side effects

## Refactor

Prefer small transformations:

1. Extract method
2. Rename
3. Extract class
4. Remove duplication
5. Improve dependency boundaries
6. Simplify control flow

## Tests

Tests should pass before and after each major transformation.

## Never

Do not combine a large refactor with unrelated feature changes unless explicitly requested.

## Final Review

Compare behavior and public interfaces.

Confirm:

- no unintended API changes
- no database behavior changes
- no authentication changes
- no configuration changes