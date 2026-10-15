# 09 — DevSecOps Scanning

## Learning Objectives
- Integrate security checks into CI early and consistently.
- Produce actionable vulnerability feedback for developers.

## Concepts
- SAST: Semgrep.
- Secrets scan: Gitleaks.
- Dependency security: `pip-audit`, Dependency Review.
- Container scan: Trivy.
- Docker linting: Hadolint.
- SARIF upload and code scanning visibility.
- Pin third-party actions to full commit SHA and use least-privilege permissions.

## Practical Exercises
- Add scan workflows in `workflows/`.
- Keep SARIF outputs/examples in `sarif/`.
- Write scan triage notes in `docs/`.

## Interview + Troubleshooting
- How do you triage scanner false positives?
- Why pin actions to full commit SHAs?
- Debug missing SARIF or failed upload scenarios.

## Completion Checklist
- [ ] I drafted workflows for Semgrep, Trivy, Gitleaks, pip-audit, Dependency Review, and Hadolint.
- [ ] I configured SARIF reporting flow.
- [ ] I enforced least-privilege workflow permissions.
