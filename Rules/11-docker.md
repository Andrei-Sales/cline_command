# Docker Rules

Docker images must be reproducible, secure, and reasonably small.

## Dockerfile

Prefer:

- multi-stage builds
- minimal runtime images
- non-root users
- explicit versions
- .dockerignore

Avoid:

- secrets in Dockerfiles
- unnecessary packages
- running as root
- copying unnecessary files

## Build

Build should be deterministic when practical.

Example:

docker build -t application:local .

## Runtime

Configuration should come from environment/configuration rather than rebuilding the image.

## Security

Never include:

- credentials
- private keys
- .env files containing secrets
- local development secrets

## Debugging

When a container fails:

1. Inspect logs.
2. Inspect exit code.
3. Inspect environment.
4. Inspect mounted files.
5. Inspect networking.
6. Reproduce locally.
7. Change one variable at a time.