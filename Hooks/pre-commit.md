# Pre-Commit Hook

Before committing:

- git status
- inspect diff
- run relevant tests
- run build
- run lint/static analysis
- check for secrets
- check for debug statements
- check generated files

Never commit:

.env
credentials
private keys
tokens
passwords
temporary debug code