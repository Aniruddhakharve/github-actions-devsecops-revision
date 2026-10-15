# 04 — Variables, Secrets, and Outputs

## Learning Objectives
- Pass data safely across steps and jobs.
- Use secrets and environment variables correctly.

## Concepts
- `env`, repository/org/environment variables.
- GitHub Secrets and masking behavior.
- Job outputs and expression contexts.

## Practical Exercises
- Draft output passing examples in `workflows/`.
- Add safe variable usage snippets in `examples/`.
- Capture secret-handling notes in `docs/`.

## Interview + Troubleshooting
- Difference between `vars`, `env`, and `secrets`?
- Why is an output empty in a downstream job?
- Debug expression/context resolution errors.

## Completion Checklist
- [ ] I can pass outputs between jobs.
- [ ] I avoid hardcoded sensitive data.
- [ ] I documented secure variable practices.
