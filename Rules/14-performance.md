# Performance Rules

Do not optimize based solely on intuition.

## First

Identify:

- bottleneck
- workload
- expected behavior
- actual measurements when available

## Backend

Check:

- database queries
- network calls
- serialization
- memory usage
- CPU usage
- thread pools
- connection pools

## Frontend

Check:

- bundle size
- rendering
- API calls
- image sizes
- unnecessary state updates

## Database

Check:

- indexes
- query plans
- N+1 queries
- full table scans
- pagination
- connection usage

## Caching

Introduce caching only when:

- data access is expensive
- consistency requirements are understood
- invalidation strategy exists

Remember:

"Cache invalidation" is part of the feature design.

## Rule

Prefer measurable improvements over speculative micro-optimizations.