# 03 — Runners, Jobs, and Steps

## Learning Objectives
- Understand where workflows run and how jobs are scheduled.
- Build multi-job pipelines with dependencies.

## Concepts
- GitHub-hosted vs self-hosted runners.
- `needs`, job parallelism, `if` conditions.
- Step outputs, shell commands, and reusable scripts.

## Practical Exercises
- Add multi-job workflows in `workflows/`.
- Keep helper scripts in `scripts/`.
- Record runner decisions and trade-offs in `docs/`.

## Interview + Troubleshooting
- How do job dependencies affect execution order?
- What causes runner label mismatch failures?
- Debug step failures with logs and exit codes.

## Completion Checklist
- [ ] I can design dependent and parallel jobs.
- [ ] I understand runner selection trade-offs.
- [ ] I practiced failure isolation per job.
