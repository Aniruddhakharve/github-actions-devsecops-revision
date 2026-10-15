# 05 — Artifacts, Cache, and Matrix

## Learning Objectives
- Improve pipeline speed and visibility.
- Validate builds across multiple versions/environments.

## Concepts
- Artifact upload/download patterns.
- Dependency caching keys and restore strategies.
- Matrix builds (`strategy.matrix`) and fail-fast control.

## Practical Exercises
- Create matrix workflow drafts in `workflows/`.
- Add cache key experiments in `examples/`.
- Track performance observations in `docs/`.

## Interview + Troubleshooting
- Artifact vs cache: when to use each?
- Why does cache miss unexpectedly?
- Debug matrix job expansion and failures.

## Completion Checklist
- [ ] I can configure reliable cache keys.
- [ ] I used artifacts for cross-job outputs/logs.
- [ ] I ran at least one matrix scenario.
