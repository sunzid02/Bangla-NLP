# WORKFLOW_RUN.md — The `RUN` Command

This file defines what to do when the user says **`RUN`**.

## On `RUN`, do this:

1. Read `CLAUDE.md`.
2. Read `WORKFLOW_RUN.md` (this file).
3. Read `PROJECT_STATUS.md`.
4. Identify the next pending action (from `PROJECT_STATUS.md` → Next Recommended Action).
5. Execute only the next safe step.
6. Do not spawn subagents unless the user explicitly asks.
7. Use `AGENTS.md` only when project rules are needed.
8. Use `docs/` only when a specific rule is needed.
9. Use `.claude/skills/` only when a specific task helper is needed.
10. Do not update `artifacts/` unless the current batch has been approved.
11. Update `PROJECT_STATUS.md` at the end of every run.
12. End with a short summary and the next recommended action.

## Low-Token Rules

- Do not reconstruct project progress from old chats.
- Do not scan all logs unless needed.
- Do not open all PDFs unless needed.
- Use `PROJECT_STATUS.md` as the main memory.
- Prefer sequential execution.
- Avoid general-purpose subagents.
- Prefer `rg`, `head`, `tail`, `ls`, and small targeted reads over loading large files.
