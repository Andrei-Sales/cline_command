# AWS Engineering Rules

Follow AWS least-privilege principles.

## Credentials

Never hardcode AWS credentials.

Prefer:

- IAM roles
- workload identity
- IRSA
- AWS Secrets Manager
- environment/configuration provided by the runtime

## IAM

Grant only required permissions.

Avoid:

Action: "*"
Resource: "*"

unless explicitly justified.

## Common Services

When working with:

EC2
EKS
S3
CloudFront
ECR
Secrets Manager
CloudWatch
CloudTrail
Lambda

inspect existing infrastructure before creating new resources.

## S3

Consider:

- bucket policies
- encryption
- public access blocking
- lifecycle policies
- least privilege

Never make buckets public simply to fix access problems without understanding the requirement.

## Secrets Manager

Do not print retrieved secrets to logs.

Cache secrets appropriately when supported.

Handle secret retrieval failures gracefully.

## CloudWatch

Use meaningful:

- log groups
- metrics
- alarms
- structured logs

## AWS Changes

Before infrastructure changes identify:

- blast radius
- dependencies
- rollback strategy
- cost implications
- security implications