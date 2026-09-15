# Code Quality Rules

Write production-quality code.

## Readability

Prefer:

- descriptive names
- small focused functions
- single responsibility
- explicit control flow
- clear error handling

Avoid:

- deeply nested conditionals
- giant functions
- unnecessary one-liners
- magic numbers
- unexplained constants
- duplicated business logic
- premature abstractions

## Functions

Functions should generally:

- do one logical thing
- have predictable inputs/outputs
- avoid hidden side effects
- handle errors explicitly

## Error Handling

Never silently swallow errors.

Bad:

try {
    operation();
} catch (Exception e) {
}

Good:

try {
    operation();
} catch (Exception e) {
    logger.error("Failed to execute operation", e);
    throw e;
}

## Logging

Logs should provide enough context to troubleshoot failures.

Do not log:

- passwords
- tokens
- API keys
- secrets
- authentication headers
- sensitive personal information

Use appropriate log levels:

- DEBUG: development diagnostics
- INFO: important application events
- WARN: recoverable abnormal conditions
- ERROR: failures requiring investigation

## Comments

Comments should explain WHY, not WHAT.

Avoid comments that simply restate code.

Prefer:

// Retry because the external service occasionally returns transient 503 responses.

over:

// Loop three times.