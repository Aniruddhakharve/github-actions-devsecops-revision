# 06 — Docker CI/CD

## Learning Objectives
- Build, test, tag, scan, and publish container images correctly.
- Apply immutable image promotion strategy.

## Concepts
- Docker build contexts, tags, and metadata.
- Registry login with placeholders only.
- Immutable tagging with commit SHA.

## Practical Exercises
- Keep workflow drafts in `workflows/`.
- Put Dockerfiles in `docker/` and sample app code in `app/`.
- Add helper deployment/build scripts in `scripts/`.
- Log image lifecycle notes in `docs/`.

## Interview + Troubleshooting
- Why is SHA-based tagging safer than `latest`?
- How do you ensure the scanned image is the deployed one?
- Debug image push/tag mismatch issues.

## Completion Checklist
- [ ] I can build image once and tag with commit SHA.
- [ ] I can scan that exact image before publish/deploy.
- [ ] I avoid rebuilding a different image later.
