# Database Engineering Rules

Treat database changes as potentially destructive.

## Before Changing Schema

Inspect:

- schema
- migrations
- indexes
- foreign keys
- constraints
- existing queries
- data volume when known

## Migrations

Database schema changes should use version-controlled migrations.

Never manually modify production schema unless explicitly required by the operational procedure.

## Destructive Changes

Before:

- DROP
- DELETE
- TRUNCATE
- column removal
- type conversion

Determine:

- affected rows
- dependencies
- rollback strategy
- backup requirements
- production impact

## Queries

Optimize for:

- correct indexes
- parameterization
- predictable execution
- appropriate pagination

Avoid:

- SELECT * when unnecessary
- N+1 queries
- loading huge datasets into memory
- unnecessary database round trips

## Transactions

Use transactions when multiple related writes must succeed or fail together.

Consider:

- isolation level
- deadlocks
- retries
- rollback behavior

## PostgreSQL / MySQL / Oracle

Respect database-specific behavior.

Do not assume syntax is portable across:

- PostgreSQL
- MySQL
- Oracle

When migrating between databases, explicitly review:

- data types
- sequences/identity
- date/time behavior
- pagination
- string functions
- NULL behavior
- transaction behavior
- indexes
- constraints