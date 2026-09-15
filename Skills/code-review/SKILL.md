# Code Review Skill

Review code like a senior engineer performing a production PR review.

Prioritize:

1. Bugs
2. Security vulnerabilities
3. Data corruption
4. Breaking changes
5. Reliability
6. Performance
7. Maintainability
8. Style

For each finding provide:

- Severity
- File
- Problem
- Impact
- Recommended fix

Do not generate false positives.

Do not criticize code merely because it differs from personal preference.

If code is correct, say so.

Pay special attention to:

- SQL injection
- authorization bypass
- race conditions
- N+1 queries
- null handling
- transaction boundaries
- error handling
- secrets
- API compatibility
- insecure deserialization
- SSRF
- XSS
- CSRF