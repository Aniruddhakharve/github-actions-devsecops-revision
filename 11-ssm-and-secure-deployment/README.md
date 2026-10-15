# 11 — SSM and Secure Deployment

## Learning Objectives
- Execute secure deployments to EC2 through SSM.
- Use Secrets Manager and health checks safely.

## Concepts
- AWS Systems Manager Run Command / Session Manager patterns.
- Runtime secret retrieval from Secrets Manager.
- Post-deploy health checks and rollback signals.
- Deployment troubleshooting for host, permissions, and service startup.

## Practical Exercises
- Draft deployment workflows in `workflows/`.
- Keep command/deploy specs in `deployment-spec/`.
- Store troubleshooting runbooks in `docs/`.

## Interview + Troubleshooting
- Why prefer SSM over direct SSH in pipelines?
- How do you verify deployment health safely?
- Debug failed SSM command execution and service startup.

## Completion Checklist
- [ ] I designed an SSM-based deployment flow.
- [ ] I added Secrets Manager retrieval pattern notes.
- [ ] I documented health-check and rollback troubleshooting.
