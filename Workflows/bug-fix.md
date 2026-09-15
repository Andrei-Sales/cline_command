# Bug Fix Workflow

Do not immediately modify code.

## Step 1 — Reproduce

Determine:

- expected behavior
- actual behavior
- reproduction steps
- affected environment

## Step 2 — Trace

Trace the execution path:

Request
→ Controller
→ Service
→ Repository
→ Database
→ External service
→ Response

or the equivalent architecture.

## Step 3 — Find Root Cause

Do not fix symptoms if the root cause can be identified.

Check:

- logs
- exceptions
- stack traces
- database state
- API responses
- frontend state
- configuration
- dependency behavior

## Step 4 — Regression Test

Create a test reproducing the failure when practical.

## Step 5 — Fix

Implement the smallest safe fix.

## Step 6 — Validate

Run:

- regression test
- related tests
- build
- lint/static analysis

## Step 7 — Review

Ensure the fix does not introduce:

- security issues
- breaking behavior
- race conditions
- performance regressions