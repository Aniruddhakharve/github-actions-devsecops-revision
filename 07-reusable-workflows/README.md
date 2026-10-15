# 07 — Reusable Workflows

## Learning Objectives
- Reduce duplication with shared workflow logic.
- Standardize CI checks across multiple pipelines.

## Concepts
- `workflow_call`, inputs, secrets inheritance.
- Caller workflow vs reusable workflow responsibilities.
- Versioning reusable workflow references.

## Practical Exercises
- Store caller workflows in `workflows/`.
- Store reusable templates in `reusable-workflows/`.
- Capture adoption guidelines in `docs/`.

## Interview + Troubleshooting
- Composite action vs reusable workflow?
- Why are inputs or secrets not passing correctly?
- Debug `uses:` path/reference issues.

## Completion Checklist
- [ ] I created at least one reusable workflow template.
- [ ] I consumed it from a caller workflow.
- [ ] I documented input/secret contracts.
