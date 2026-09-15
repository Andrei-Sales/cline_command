# Java Backend Rules

Follow the existing Java architecture.

## Maven

Before modifying dependencies:

- inspect pom.xml
- check existing dependency versions
- avoid duplicate libraries

Prefer Maven lifecycle commands appropriate to the project.

Typical validation:

mvn test
mvn verify
mvn package

## Java

Prefer:

- immutable data where appropriate
- clear interfaces
- dependency injection
- small services
- explicit exception handling

Avoid:

- giant service classes
- unnecessary inheritance
- static global state
- catching Exception without reason

## Null Handling

Prefer clear null-handling strategies.

Use Optional where it improves API clarity, not everywhere.

## Exceptions

Use domain-specific exceptions when appropriate.

Do not expose internal exceptions directly through APIs.

## Transactions

Ensure transaction boundaries are clearly defined.

## Concurrency

When working with concurrent code, explicitly consider:

- thread safety
- shared mutable state
- race conditions
- deadlocks
- synchronization

## Legacy Java

If the project uses older Java patterns:

- follow existing conventions
- modernize incrementally
- avoid introducing incompatible language features without checking build/runtime versions