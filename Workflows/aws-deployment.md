# AWS Deployment Workflow

Use for application deployments to AWS.

## Step 1

Identify deployment architecture.

Example:

React
→ CloudFront/S3
→ API
→ EKS
→ Database

or:

Client
→ CloudFront
→ ALB
→ EKS
→ PostgreSQL

## Step 2

Inspect:

- Dockerfile
- Kubernetes manifests
- Helm charts
- Terraform
- GitHub Actions
- CodePipeline
- ECR
- Secrets Manager
- IAM

## Step 3

Build

Run tests and build application.

## Step 4

Container

Build image and verify:

- image starts
- health endpoint works
- configuration works
- secrets are not included

## Step 5

Push

Push image to ECR using the existing CI/CD process.

## Step 6

Deploy

Deploy using the existing project's deployment mechanism.

## Step 7

Verify

Check:

- rollout
- pods
- logs
- health probes
- ingress/load balancer
- application endpoint
- CloudWatch

## Step 8

Rollback

If health checks fail or errors increase:

- stop
- identify cause
- rollback when appropriate
- document the failure