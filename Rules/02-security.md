# Security Rules

Security is mandatory.

## Secrets

Never hardcode:

- passwords
- API keys
- access tokens
- private keys
- database credentials
- JWT secrets
- encryption keys

Use appropriate configuration mechanisms such as:

- environment variables
- AWS Secrets Manager
- Kubernetes Secrets
- secret managers supported by the deployment platform

Never commit secrets to Git.

## Input Validation

Treat all external input as untrusted.

Validate:

- HTTP parameters
- request bodies
- headers
- uploaded files
- query parameters
- database input
- messages from queues

## SQL

Always use parameterized queries/prepared statements.

Never construct SQL using raw user input.

Bad:

"SELECT * FROM users WHERE id = " + userId

Good:

PreparedStatement / parameterized query.

## Authentication

Never implement custom cryptography unless absolutely necessary.

Use established:

- OAuth2
- OpenID Connect
- Azure AD / Microsoft Entra ID
- JWT libraries
- framework security mechanisms

## Authorization

Authentication answers:

"Who are you?"

Authorization answers:

"Are you allowed to do this?"

Always enforce authorization server-side.

Never rely only on frontend UI restrictions.

## Web Security

Consider:

- SQL injection
- XSS
- CSRF
- SSRF
- path traversal
- insecure deserialization
- broken access control
- authentication bypass
- insecure file uploads
- mass assignment

## Dependencies

Before adding a dependency:

1. Determine whether the existing project already provides equivalent functionality.
2. Prefer maintained and reputable packages.
3. Avoid unnecessary dependencies.
4. Consider licensing and known security vulnerabilities.

## Sensitive Data

Do not expose sensitive data through:

- logs
- error responses
- frontend JavaScript
- URLs
- Git
- Docker images
- Kubernetes manifests