# GitHub Actions + DevSecOps Revision Lab

Hands-on revision workspace for **Day 38–49 topics**: GitHub Actions, CI/CD, Docker, and DevSecOps.

> This repository is intentionally a **learning and revision sandbox** (not a production clone of your Secure CI/CD Pipeline Lab).

## Goals

- Rebuild CI/CD fundamentals through short practical exercises.
- Practice writing and debugging workflow YAML files.
- Learn secure pipeline patterns for code, dependency, and image scanning.
- Prepare for interviews with targeted Q&A and troubleshooting drills.

## Learning Roadmap

1. [01 YAML + CI/CD Fundamentals](./01-yaml-cicd-fundamentals/README.md)
2. [02 Workflows and Triggers](./02-workflows-and-triggers/README.md)
3. [03 Runners, Jobs, and Steps](./03-runners-jobs-and-steps/README.md)
4. [04 Variables, Secrets, and Outputs](./04-variables-secrets-and-outputs/README.md)
5. [05 Artifacts, Cache, and Matrix](./05-artifacts-cache-and-matrix/README.md)
6. [06 Docker CI/CD](./06-docker-ci-cd/README.md)
7. [07 Reusable Workflows](./07-reusable-workflows/README.md)
8. [08 Advanced Triggers](./08-advanced-triggers/README.md)
9. [09 DevSecOps Scanning](./09-devsecops-scanning/README.md)
10. [10 AWS OIDC and IAM](./10-aws-oidc-and-iam/README.md)
11. [11 SSM and Secure Deployment](./11-ssm-and-secure-deployment/README.md)
12. [12 Capstone Revision](./12-capstone-revision/README.md)

## Topics Covered

- GitHub Actions basics: YAML syntax, workflow structure, jobs, steps, expressions, contexts.
- Trigger design: push, pull_request, workflow_dispatch, schedule, path filters, branch filters.
- Runners and execution model: hosted/self-hosted, dependencies, outputs, job orchestration.
- Data flow: variables, environment variables, secrets, and cross-job outputs.
- Performance and scale: artifacts, dependency caching, matrix builds.
- Docker CI/CD: build/test/push patterns, tagging strategy, immutable artifact promotion.
- Reusable workflows and maintainability patterns.
- Advanced trigger and debugging scenarios.
- DevSecOps scanners: **Semgrep, Trivy, Gitleaks, pip-audit, Dependency Review, Hadolint, SARIF reporting**.
- Security hygiene: least-privilege permissions, third-party actions pinned to full commit SHA.
- AWS secure delivery: OIDC, STS temporary credentials, IAM trust policies, deployment vs EC2 runtime roles, SSM-based deployment, Secrets Manager, health checks, rollback troubleshooting.

## Important Practical Principle

Always follow this flow:
1. **Build image once**
2. **Scan that exact image**
3. **Promote/deploy the same image** tagged with immutable commit SHA (for example `<registry>/<app>:<git-sha>`)

Avoid rebuilding a different image later in the pipeline.

## Repository Structure

```text
github-actions-devsecops-revision/
├── README.md
├── 01-yaml-cicd-fundamentals/
├── 02-workflows-and-triggers/
├── 03-runners-jobs-and-steps/
├── 04-variables-secrets-and-outputs/
├── 05-artifacts-cache-and-matrix/
├── 06-docker-ci-cd/
├── 07-reusable-workflows/
├── 08-advanced-triggers/
├── 09-devsecops-scanning/
├── 10-aws-oidc-and-iam/
├── 11-ssm-and-secure-deployment/
└── 12-capstone-revision/
```

Each numbered folder includes:
- `README.md` (phase objective + checklist)
- `workflows/` (workflow YAML drafts)
- supporting folders (`examples/`, `scripts/`, `docs/`, etc.) for focused hands-on practice

Use placeholders such as `<aws-account-id>`, `<role-arn>`, `<registry-user>`, `<repository-name>` until environment values are available.

## Revision Progress Checklist

- [ ] 01 YAML + CI/CD fundamentals completed
- [ ] 02 Workflows and triggers completed
- [ ] 03 Runners, jobs, and steps completed
- [ ] 04 Variables, secrets, and outputs completed
- [ ] 05 Artifacts, cache, and matrix completed
- [ ] 06 Docker CI/CD completed
- [ ] 07 Reusable workflows completed
- [ ] 08 Advanced triggers completed
- [ ] 09 DevSecOps scanning completed
- [ ] 10 AWS OIDC and IAM completed
- [ ] 11 SSM and secure deployment completed
- [ ] 12 Capstone revision completed

## How to Use This Repo

1. Work one phase at a time.
2. Add/modify workflow YAML files in that phase.
3. Test and debug incrementally.
4. Mark checklist items only after you run and verify them.
5. Keep security settings and permissions explicit and minimal.
