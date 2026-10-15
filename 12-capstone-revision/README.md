# 12 — Capstone Revision

## Learning Objectives
- Connect all phases into a coherent secure CI/CD story.
- Practice interview-style explanation of design decisions.

## Concepts
- End-to-end pipeline flow mapping.
- Security gates placement and justification.
- Immutable artifact/image promotion with commit SHA.
- Practical trade-offs: speed, security, maintainability.

## Practical Exercises
- Draft integrated workflows in `workflows/`.
- Write final runbooks and reflection notes in `runbooks/`.
- Keep final revision summaries in `docs/`.

## Interview + Troubleshooting
- Walk through your end-to-end secure pipeline design.
- Explain where each scanner runs and why.
- Diagnose a failed release with CI + deployment signals.

## Completion Checklist
- [ ] I can explain the full CI/CD + DevSecOps flow clearly.
- [ ] I can justify scanner placement and IAM boundaries.
- [ ] I validated the build-once, scan-once, deploy-same-image principle.
