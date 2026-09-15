# Node.js Backend Rules

Follow the existing Node.js architecture.

## Async Code

Prefer async/await for asynchronous workflows.

Always handle rejected promises.

## API

Validate request:

- body
- query
- params
- headers

Use the project's existing validation library when available.

## Errors

Centralize error handling when architecture supports it.

Never expose stack traces or internal implementation details to production clients.

## Dependencies

Before adding npm packages:

- inspect package.json
- check whether functionality already exists
- consider maintenance and security
- avoid unnecessary dependencies

## Environment

Use environment variables for deployment-specific configuration.

Never hardcode:

- credentials
- tokens
- database passwords

## Database

Use parameterized queries or the project's ORM/query builder.

Avoid N+1 queries.

## Logging

Use structured logging when supported by the application.

Never log secrets.