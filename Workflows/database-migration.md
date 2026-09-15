# Database Migration Workflow

Use when migrating or modifying databases.

## Phase 1

Inventory:

- tables
- columns
- indexes
- constraints
- sequences
- triggers
- stored procedures
- jobs
- application queries

## Phase 2

Identify incompatibilities.

For Oracle → PostgreSQL, inspect:

- NUMBER → numeric/integer
- VARCHAR2 → varchar
- DATE/TIMESTAMP behavior
- sequences
- NVL
- DECODE
- ROWNUM
- CONNECT BY
- PL/SQL
- stored procedures
- packages
- MERGE
- pagination
- case sensitivity

For MySQL → PostgreSQL inspect:

- AUTO_INCREMENT
- backticks
- LIMIT syntax
- boolean behavior
- date functions
- JSON
- ENUM
- collations

## Phase 3

Create migration scripts.

## Phase 4

Test against realistic data.

## Phase 5

Validate:

- row counts
- checksums where appropriate
- constraints
- indexes
- application behavior
- performance

## Phase 6

Document rollback strategy.