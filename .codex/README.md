# Codex Research Team Setup

This project uses the main Codex thread as the Lead Researcher and keeps the focused specialists as subagents under `.codex/agents/`.

Included subagents:

- `bioinformatics_analyst`
- `senior_scientist`

Main-thread instructions:

- The Lead Researcher behavior is defined in the repository root `AGENTS.md`.
- This follows the Codex guidance to use `AGENTS.md` for project instructions for the main session.

Notes:

- `bioinformatics_analyst` is the only agent here with `sandbox_mode = "workspace-write"`.
- `senior_scientist` is set to `read-only` because it is primarily an interpretation and literature role.

Example prompt:

Plan the next analysis steps for this project. Use `bioinformatics_analyst` to execute the top-priority computational analysis, then ask `senior_scientist` to interpret the result in the context of published literature.
