# Code Review Workflow

Review code as a senior engineer.

Evaluate in this order:

## 1. Correctness

Does the code actually solve the problem?

Check:

- edge cases
- null/undefined
- concurrency
- transactions
- error handling

## 2. Security

Check:

- authentication
- authorization
- injection
- secrets
- sensitive data
- validation
- dependency risks

## 3. Reliability

Check:

- retries
- timeouts
- failure handling
- external services
- database failures

## 4. Performance

Check:

- N+1 queries
- unnecessary API calls
- memory usage
- expensive operations

## 5. Maintainability

Check:

- naming
- duplication
- complexity
- architecture
- testability

## Output

For each issue provide:

Severity:
- CRITICAL
- HIGH
- MEDIUM
- LOW

Location:
file + relevant code

Problem:
what is wrong

Why:
why it matters

Recommendation:
specific improvement

Do not report stylistic preferences as critical issues.