# GitHub Actions + DevSecOps — Master Revision Plan

> **Purpose:** This is the source of truth for our revision sequence. We will follow the topics in order, one concept at a time, and update the progress and **Next Topic** section after each revision session.
>
> **Reference material:** Day 38–49 README files and personal notes in the `90DaysOfDevOps-shubham-londe/2026` repository, plus the `Secure CI/CD Pipeline Lab`.
>
> **Practice repository:** https://github.com/Aniruddhakharve/github-actions-devsecops-revision

---

## How we will study

For each concept, follow this learning cycle:

1. **Understand:** beginner-friendly explanation, purpose, and the problem it solves.
2. **Connect:** how it fits into GitHub Actions, CI/CD, Docker, DevSecOps, or AWS architecture.
3. **Compare:** relevant alternatives, differences, trade-offs, and common confusions.
4. **Practice:** write or modify the YAML, command, policy, or configuration in this repository.
5. **Troubleshoot:** inspect a failure or scenario and explain how to diagnose it.
6. **Interview:** answer relevant interview questions in your own words.
7. **Record:** update this plan and the relevant phase README with what was completed and what comes next.

**Completion rule:** A topic is not complete merely because it was explained. Mark it complete when you can explain it back and complete the applicable practical exercise. If a topic needs more practice, keep it open and continue it before moving forward.

We will not rush, skip concepts, or mark work complete without verification. If a session ends halfway through a topic, record the exact next subtopic below.

---

# Revision roadmap — 14 sessions

## Session 1 — YAML fundamentals and CI/CD foundations

- [ ] YAML purpose and where it is used in GitHub Actions
- [ ] Key-value pairs, mappings/objects, lists/sequences, nested structures
- [ ] Indentation rules; spaces vs tabs
- [ ] Strings, numbers, booleans, quoting and special characters
- [ ] Multiline strings: literal block `|` vs folded block `>`
- [ ] YAML comments and basic document structure
- [ ] Common YAML syntax and indentation errors
- [ ] YAML validation and linting with `yamllint`
- [ ] What is CI/CD and why teams use it
- [ ] Continuous Integration vs Continuous Delivery vs Continuous Deployment
- [ ] Typical pipeline stages and pipeline anatomy
- [ ] Map a simple CI/CD pipeline to a real software project

**Practical:** Write sample YAML structures, validate them, and document common mistakes.

## Session 2 — GitHub Actions fundamentals and first workflow

- [ ] What GitHub Actions is and where it fits in CI/CD
- [ ] Workflow, event/trigger, job, step, runner, action
- [ ] `.github/workflows/` directory and workflow file extensions
- [ ] Workflow top-level structure: `name`, `on`, `permissions`, `jobs`
- [ ] `runs-on`, `steps`, `run`, and `uses`
- [ ] Difference between running shell commands and using an action
- [ ] Checking out repository code with `actions/checkout`
- [ ] Workflow execution, logs, status and run history
- [ ] GitHub-provided environment variables (introductory use)
- [ ] Intentionally failing a step and reading the logs
- [ ] Basic workflow debugging process

**Practical:** Create a first workflow, trigger it, inspect its run, introduce a controlled failure, and fix it.

## Session 3 — Workflow triggers, filters and pull-request validation

- [ ] Event-driven workflow execution
- [ ] `push` trigger
- [ ] `pull_request` trigger
- [ ] Pull request lifecycle and relevant activity types
- [ ] `types`: `opened`, `synchronize`, `reopened`, `closed`, etc.
- [ ] Branch filters: `branches` and `branches-ignore`
- [ ] Path filters: `paths` and `paths-ignore`
- [ ] Tag filters (where relevant)
- [ ] `workflow_dispatch` and manual execution
- [ ] Manual workflow inputs and input types
- [ ] `schedule` trigger and cron expression syntax
- [ ] UTC scheduling considerations
- [ ] PR validation examples: branch naming, PR title/body, changed files and file-size checks
- [ ] Choosing the right event for a task
- [ ] Debugging why a workflow did not trigger

**Practical:** Create and test push, PR, manual and scheduled trigger examples, including branch/path filters.

## Session 4 — Runners, jobs and steps

- [ ] What a runner does
- [ ] GitHub-hosted runners
- [ ] Self-hosted runners
- [ ] Linux, Windows and macOS runner choices
- [ ] Runner labels and `runs-on`
- [ ] Runner environment and preinstalled software
- [ ] Self-hosted runner security, isolation, maintenance and cleanup considerations
- [ ] Jobs and steps: responsibilities and differences
- [ ] Default job parallelism
- [ ] Sequential steps inside a job
- [ ] Job dependencies using `needs`
- [ ] Parallel vs sequential job execution
- [ ] Job-level and step-level conditions (intro)
- [ ] Exit codes and how step failure affects a job

**Practical:** Build a multi-job workflow with parallel jobs and a dependent job.

## Session 5 — Variables, contexts, expressions and conditions

- [ ] Workflow-, job- and step-level `env`
- [ ] Environment-variable scope and precedence/overriding
- [ ] Default GitHub environment variables
- [ ] GitHub contexts and when to use them
- [ ] `github`, `env`, `vars`, `secrets`, `steps`, `needs`, and `runner` contexts
- [ ] Expression syntax: `${{ ... }}`
- [ ] Expressions vs shell variable expansion
- [ ] Referencing event and repository information
- [ ] `if` conditions on jobs and steps
- [ ] `success()`, `failure()`, `always()`, and `cancelled()`
- [ ] Conditional execution and status-check behavior
- [ ] `continue-on-error`
- [ ] Common expression and context mistakes

**Practical:** Pass values through environment variables, inspect contexts, and conditionally execute steps/jobs.

## Session 6 — Outputs, job dependencies, matrix and failure handling

- [ ] Step outputs
- [ ] Writing step outputs using `$GITHUB_OUTPUT`
- [ ] Job outputs and mapping step outputs to job outputs
- [ ] Reading outputs from downstream jobs using `needs`
- [ ] Difference between environment variables, step outputs and job outputs
- [ ] Job dependency graph and execution order
- [ ] Matrix strategy and matrix expansion
- [ ] Testing multiple language/runtime versions
- [ ] Testing across operating systems
- [ ] Matrix `include` and `exclude`
- [ ] `fail-fast` and `max-parallel`
- [ ] Failure, skipped and cancelled job behavior
- [ ] Debugging a failed matrix combination

**Practical:** Build a matrix test workflow and pass a generated value from one job to another.

## Session 7 — Secrets, variables, artifacts, cache and test reports

- [ ] GitHub repository, organization and environment secrets
- [ ] GitHub Actions variables vs secrets
- [ ] Referencing secrets safely with the `secrets` context
- [ ] Passing secrets to steps and reusable workflows
- [ ] Secret masking limitations and why secrets must never be printed
- [ ] Avoiding hardcoded credentials in source code and workflow files
- [ ] `$GITHUB_ENV` vs `$GITHUB_OUTPUT`
- [ ] Workflow artifacts and their purpose
- [ ] Uploading and downloading artifacts
- [ ] Sharing build outputs/reports between jobs
- [ ] Artifacts vs dependency cache
- [ ] Cache keys, restore keys and cache misses
- [ ] Dependency caching and when caching is appropriate
- [ ] Test reports and build outputs

**Practical:** Run tests, cache dependencies, upload an artifact and download it in another job.

## Session 8 — Docker CI/CD and image publishing

- [ ] Docker build in GitHub Actions
- [ ] Docker build context and Dockerfile location
- [ ] Docker image names, tags and registries
- [ ] Docker Hub authentication and `docker/login-action`
- [ ] `docker/build-push-action` and Buildx (purpose and usage)
- [ ] Build vs push behavior
- [ ] `latest` tag vs immutable commit-SHA tag
- [ ] Tagging images with commit SHA
- [ ] Publishing only from approved branches/events
- [ ] PR validation without publishing a production image
- [ ] Pulling and running the published image
- [ ] GitHub Actions status badges
- [ ] Diagnosing Docker build, authentication, tag and push failures

**Practical:** Build and publish a practice image using safe placeholders/secrets; verify the image by pulling and running it.

## Session 9 — Reusable workflows and composite actions

- [ ] Why workflow reuse matters
- [ ] Reusable workflow concept
- [ ] `workflow_call` trigger
- [ ] Caller workflow vs called/reusable workflow
- [ ] Reusable workflow location and reference syntax
- [ ] Inputs, types, required values and defaults
- [ ] Passing secrets to reusable workflows
- [ ] `secrets: inherit` and its implications
- [ ] Outputs from reusable workflows
- [ ] Permissions and runner considerations
- [ ] Composite actions: purpose and structure
- [ ] Composite actions vs reusable workflows
- [ ] Reusable workflow version/reference considerations
- [ ] `workflow_call` vs `workflow_run`
- [ ] Troubleshooting input, secret, output and reference errors

**Practical:** Create a reusable test workflow and call it from another workflow.

## Session 10 — Advanced triggers and workflow coordination

- [ ] Pull-request activity types and event payloads
- [ ] `workflow_run`: purpose, completion event and workflow chaining
- [ ] `repository_dispatch`: external/custom event triggering
- [ ] Event payloads and relevant GitHub context values
- [ ] Scheduled automation and health-check workflows
- [ ] Trigger filters and conditions in more complex workflows
- [ ] Workflow chaining and coordination
- [ ] Avoiding unintended repeated workflow runs
- [ ] Concurrency groups and cancellation behavior
- [ ] Choosing between normal triggers, `workflow_run` and `repository_dispatch`
- [ ] Troubleshooting unexpected, duplicate or missing workflow runs

**Practical:** Create examples for at least two advanced triggers and document their event flow.

## Session 11 — End-to-end CI/CD workflow design

- [ ] Design a PR validation pipeline
- [ ] Design a main-branch CI/CD pipeline
- [ ] Separate test, build, scan, publish and deployment stages
- [ ] Job dependencies and reusable workflow integration
- [ ] GitHub Environments and environment-specific configuration
- [ ] Required reviewers / deployment approval gates
- [ ] Workflow-level and job-level permissions
- [ ] Least-privilege permissions (application to workflow design)
- [ ] Workflow summaries using `$GITHUB_STEP_SUMMARY`
- [ ] Scheduled health checks
- [ ] Deployment health verification
- [ ] Status badges and readable run summaries
- [ ] End-to-end workflow troubleshooting

**Practical:** Draw and implement a small CI pipeline with PR checks, a main-branch path and a clear job dependency graph.

## Session 12 — DevSecOps scanning and pipeline hardening

- [ ] DevSecOps principles and shift-left security
- [ ] Security checks across the software delivery lifecycle
- [ ] SAST vs software composition/dependency analysis vs container scanning
- [ ] Semgrep: static application security testing
- [ ] Gitleaks: secret detection
- [ ] GitHub secret scanning and push protection
- [ ] `pip-audit`: Python dependency vulnerability auditing
- [ ] Dependency Review: pull-request dependency change review
- [ ] Dependency Review vs `pip-audit`
- [ ] Trivy: container image vulnerability scanning
- [ ] HIGH/CRITICAL severity thresholds and security gates
- [ ] Hadolint: Dockerfile linting
- [ ] SARIF format and GitHub Code Scanning upload
- [ ] Understanding and triaging findings/false positives
- [ ] Workflow `permissions` and least privilege
- [ ] Pinning third-party actions to full commit SHAs
- [ ] Why mutable action tags are a supply-chain risk
- [ ] What should block a pipeline vs what should warn

**Practical:** Add scanner workflow examples, inspect sample findings, configure a gate, and understand SARIF reporting. Do not commit real secrets or credentials.

## Session 13 — GitHub OIDC, AWS STS and IAM

- [ ] Why long-lived AWS access keys in CI/CD are risky
- [ ] Identity federation and OpenID Connect (OIDC)
- [ ] GitHub Actions OIDC identity provider
- [ ] GitHub-issued OIDC token and JWT claims (purpose)
- [ ] AWS IAM OIDC provider
- [ ] IAM role trust policy
- [ ] Trust-policy conditions for repository, branch and environment
- [ ] AWS Security Token Service (STS)
- [ ] Temporary credentials and role assumption
- [ ] GitHub Actions `id-token: write` permission
- [ ] Difference between `id-token: write` and AWS resource permissions
- [ ] `aws-actions/configure-aws-credentials` and its role in authentication
- [ ] GitHub deployment IAM role
- [ ] EC2 instance/runtime IAM role
- [ ] Separate responsibilities and permissions of the two roles
- [ ] OIDC vs STS vs IAM: how they fit together
- [ ] Troubleshooting trust-policy and `AccessDenied` errors

**Practical:** Review and explain the OIDC trust policy and the authentication flow using placeholders. Avoid creating unnecessary AWS resources.

**Flow to explain:** GitHub Actions → GitHub OIDC token → AWS STS role assumption → temporary credentials → authorized AWS API calls.

## Session 14 — SSM, Secrets Manager and secure production deployment

- [ ] AWS Systems Manager overview
- [ ] SSM Session Manager vs Run Command
- [ ] SSM-based deployment without SSH keys
- [ ] EC2 managed-node prerequisites and SSM connectivity
- [ ] EC2 instance role and required SSM permissions
- [ ] GitHub deployment role permissions for SSM operations
- [ ] AWS Secrets Manager and runtime secret retrieval
- [ ] Secrets Manager vs GitHub Secrets
- [ ] Secure handling of database credentials
- [ ] Docker and Docker Compose on the deployment server
- [ ] Deployment commands and environment configuration
- [ ] Docker Compose environment-variable interpolation
- [ ] Flask/application and MySQL service configuration
- [ ] MySQL persistent volumes and data preservation
- [ ] Application health checks and post-deployment verification
- [ ] Deployment failure diagnosis
- [ ] Rollback and recovery considerations
- [ ] Explain the full path from GitHub commit to production EC2

**Practical:** Trace and document the SSM deployment flow and health verification. Use placeholders; do not create or deploy AWS infrastructure unless we explicitly decide to do so.

---

# Capstone revision — Secure CI/CD Pipeline Lab

Use the existing [Secure CI/CD Pipeline Lab](https://github.com/Aniruddhakharve/secure-cicd-pipeline-lab) as the real project reference. This is a review of the project and its design, not a request to duplicate the full project in this revision repository.

## A. Application and containerization

- [ ] Flask application structure and request flow
- [ ] MySQL integration and database configuration
- [ ] Dockerfile and image build process
- [ ] Docker Compose services and networking
- [ ] Environment variables and `.env` handling
- [ ] MySQL persistent volume
- [ ] Local application and database testing

## B. CI/CD workflow architecture

- [ ] PR checks vs main-branch pipeline
- [ ] Reusable build/test and Docker workflows
- [ ] Workflow triggers and job dependencies
- [ ] Build Once → Scan Same Image → Push/Deploy Same Image
- [ ] Commit-SHA image tagging
- [ ] `docker save` and `docker load`
- [ ] Artifact transfer between jobs
- [ ] Why rebuilding after scanning can invalidate the scan-to-deploy guarantee
- [ ] Docker Hub publishing
- [ ] GitHub Environment approval and production deployment

## C. Security and AWS integration

- [ ] Semgrep, Gitleaks, `pip-audit`, Dependency Review
- [ ] Hadolint and Dockerfile checks
- [ ] Trivy scan and SARIF reporting
- [ ] Full-SHA action pinning
- [ ] GitHub OIDC provider and IAM trust policy
- [ ] `GitHubActions-Production-Deploy` role
- [ ] `ProductionEC2-SSM-Role`
- [ ] AWS STS temporary credentials
- [ ] SSM deployment without SSH
- [ ] Secrets Manager database credentials
- [ ] Least-privilege permissions for each role
- [ ] Production health verification

## D. Troubleshooting and interview explanation

- [ ] Diagnose workflow failures from logs
- [ ] Diagnose permissions and OIDC trust-policy failures
- [ ] Diagnose Docker build, tag, login and push failures
- [ ] Diagnose Trivy findings and security-gate failures
- [ ] Diagnose artifact and image-transfer failures
- [ ] Diagnose SSM command and IAM permission failures
- [ ] Diagnose missing secrets and database connectivity
- [ ] Diagnose application health-check failures
- [ ] Explain rollback/recovery choices
- [ ] Draw the project architecture from memory
- [ ] Explain each component and why it is needed
- [ ] Explain key security controls and design trade-offs
- [ ] Present the project end-to-end as an interview answer

---

# Final practical assessment

- [ ] Write a basic workflow from scratch without copying
- [ ] Configure push, PR and manual triggers correctly
- [ ] Build a multi-job workflow with dependencies and outputs
- [ ] Configure secrets and permissions safely
- [ ] Use artifacts and cache for the correct purposes
- [ ] Create a matrix workflow
- [ ] Build and tag a Docker image
- [ ] Explain immutable image tags and artifact promotion
- [ ] Create and call a reusable workflow
- [ ] Add a security scanner and explain its findings
- [ ] Explain the GitHub OIDC → AWS STS authentication flow
- [ ] Explain the difference between deployment and EC2 runtime IAM roles
- [ ] Explain an SSM-based deployment and health check
- [ ] Troubleshoot a deliberately broken workflow
- [ ] Explain the Secure CI/CD Pipeline Lab end-to-end
- [ ] Complete a mock interview covering the revision topics

---

# Revision continuity log — update after every session

This section is especially important when continuing in a new chat. Update it at the end of every revision session so the next chat can resume from the exact point reached.

| Field | Current value |
|---|---|
| Overall status | Not started |
| Last completed session | None |
| Last completed topic | None |
| Current session | Session 1 |
| Current topic | YAML purpose and where it is used in GitHub Actions |
| Next topic | YAML key-value pairs, mappings/objects, lists/sequences and nested structures |
| Practice repository | This repository |
| Last updated | Before Session 1 |

## Session notes

Add a short entry after each session:

- **Session/date:**
- **Concepts completed:**
- **Hands-on files created/changed:**
- **What I can explain confidently:**
- **Topics needing more practice:**
- **Exact next concept:**

## Rules for continuing in a new chat

1. Read this file first.
2. Check the continuity log and the checkboxes.
3. Check the relevant phase README and existing practice files.
4. Resume from the exact **Next topic**; do not restart completed topics or skip unfinished ones.
5. Update this file after the session, including the next concept to study.

---

## Scope notes

- The 14 sessions are a teaching sequence. The repository has 12 phase folders; multiple sessions can contribute to one phase.
- The capstone is a separate integration/revision stage, not a replacement for the 14-session concept sequence.
- We may spend more than one sitting on a session. Do not force a session to finish in one day.
- If an important gap is discovered in the original Day 38–49 notes or project, add it to the appropriate section before moving ahead.
- Keep practical examples safe: use placeholders, never commit credentials, and do not run billable AWS operations without explicit agreement.
