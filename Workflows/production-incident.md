# Production Incident Workflow

Prioritize restoration of service.

## Step 1 — Establish Impact

Determine:

- affected service
- affected users
- start time
- severity
- recent deployments

## Step 2 — Gather Evidence

Inspect:

- application logs
- CloudWatch
- Kubernetes pods
- events
- deployment history
- database health
- external dependencies

Do not make random changes.

## Step 3 — Mitigate

Prefer reversible actions:

- rollback deployment
- scale service
- disable problematic feature
- restore healthy configuration

## Step 4 — Verify

Confirm:

- application health
- error rate
- latency
- database health
- user-facing functionality

## Step 5 — Root Cause

After stabilization determine:

- technical root cause
- contributing factors
- why monitoring did not catch it
- prevention

## Step 6 — Follow-up

Create:

- regression test
- monitoring improvement
- documentation
- permanent fix