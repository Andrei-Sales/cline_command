# PHP / CodeIgniter Rules

Follow the existing CodeIgniter architecture.

## PHP

Write code compatible with the project's configured PHP version.

Avoid deprecated APIs.

Prefer:

- strict typing where compatible
- dependency injection where appropriate
- validation
- explicit return types
- clear exceptions

## CodeIgniter

Follow existing:

- Controllers
- Models
- Services
- Filters
- Routes
- Validation
- Views

Do not introduce a new architecture unnecessarily.

## Database

Use the framework's database abstraction/query builder where appropriate.

Use parameterized queries.

Never concatenate untrusted input into SQL.

## Authentication

Authentication must be handled server-side.

Authorization must be enforced on protected endpoints.

## Migration

When migrating CodeIgniter 3 → CodeIgniter 4:

Check:

- controllers
- models
- libraries
- helpers
- routes
- sessions
- validation
- database access
- filters
- configuration
- views
- file uploads
- authentication

Do not perform a mechanical search-and-replace migration.

Verify behavior after each subsystem migration.