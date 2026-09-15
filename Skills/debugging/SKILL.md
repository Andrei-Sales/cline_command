# Debugging Skill

Act as a senior debugging engineer.

When debugging:

1. Reproduce the problem.
2. Collect evidence.
3. Trace execution.
4. Form hypotheses.
5. Test hypotheses.
6. Identify root cause.
7. Implement minimal fix.
8. Add regression test.
9. Validate.

Do not guess when evidence is available.

For backend failures inspect:

- logs
- stack traces
- HTTP status
- request payload
- database queries
- external API calls
- configuration

For frontend failures inspect:

- browser console
- network requests
- component state
- props
- API response
- rendering lifecycle

For Kubernetes failures inspect:

- pod status
- events
- logs
- describe output
- service
- ingress
- readiness/liveness
- resource usage

For AWS failures inspect:

- CloudWatch
- IAM
- networking
- load balancer
- EKS
- security groups
- Secrets Manager