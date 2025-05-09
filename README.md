# DevOps IaC for OnTheGo AutoCare

This repo codifies all infrastructure in Terraform & AWS CDK, with a GitHub Actions CI/CD pipeline, and a Docker image for local tooling.

## Prerequisites

- AWS credentials with perms to assume roles / manage infra
- GitHub Secrets:
  - `AWS_ACCESS_KEY_ID`
  - `AWS_SECRET_ACCESS_KEY`
  - `AWS_DEFAULT_REGION` (defaults to `ca-central-1`)
  - `TF_STATE_BUCKET` (your S3 bucket name)
  - `TF_LOCK_TABLE` (your DynamoDB lock table name)
- Docker (optional)

## Quickstart

1. **Build the tooling image** (optional):
   ```bash
   docker build -t devops-iac:latest .
