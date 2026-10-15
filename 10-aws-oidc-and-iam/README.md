# 10 — AWS OIDC and IAM

## Learning Objectives
- Replace long-lived keys with GitHub OIDC federation.
- Design secure IAM role boundaries for CI/CD.

## Concepts
- GitHub OIDC token exchange with AWS STS temporary credentials.
- IAM trust policy conditions (repo, branch, environment).
- Separate roles for deployment automation and EC2 runtime behavior.
- Placeholder-first configuration (`<aws-account-id>`, `<deployment-role-arn>`, `<ec2-role-arn>`).

## Practical Exercises
- Draft OIDC auth workflows in `workflows/`.
- Keep trust/permission policy templates in `iam-policies/`.
- Record assumptions and constraints in `docs/`.

## Interview + Troubleshooting
- Why is OIDC safer than static AWS keys?
- How do trust policy conditions reduce blast radius?
- Debug `AccessDenied` from incorrect role trust policy.

## Completion Checklist
- [ ] I can explain OIDC to STS credential flow.
- [ ] I created trust policy templates with conditions.
- [ ] I separated deployment and EC2 runtime responsibilities.
