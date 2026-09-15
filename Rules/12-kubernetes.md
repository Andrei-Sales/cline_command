# Kubernetes Rules

Treat Kubernetes configuration as production infrastructure.

## Resources

Define resource requests/limits when appropriate.

Consider:

- CPU
- memory
- replicas
- autoscaling

## Security

Prefer:

- non-root containers
- read-only filesystems where possible
- least-privilege RBAC
- Kubernetes Secrets or external secret managers
- network policies where appropriate

## Deployments

Before modifying manifests:

Inspect:

- Deployment
- Service
- Ingress
- ConfigMap
- Secret
- HPA
- ServiceAccount
- RBAC

## Health

Use:

- readiness probes
- liveness probes
- startup probes when appropriate

## Rollout

After deployment:

- inspect rollout status
- inspect pods
- inspect events
- inspect logs
- verify service health

Never assume:

"kubectl apply succeeded"

means:

"application is healthy."

## EKS

When working with AWS EKS consider:

- IAM
- IRSA
- load balancers
- security groups
- networking
- cluster/node compatibility
- autoscaling
- CloudWatch integration