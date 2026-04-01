# Codex Agent Project Skeleton

This repository is a starter template for running a computational biology project in Codex with a clear division of labor between a lead research thread and specialist subagents.

The main Codex thread acts as the Lead Researcher. It manages project strategy, scopes analyses, tracks outputs, maintains the lab notebook, and keeps the user aligned on the next decision. Focused specialist agents live under `.codex/agents/` and handle computational execution or literature-grounded interpretation.

## Included roles

- `Lead Researcher`: the main thread, governed by `AGENTS.md`
- `bioinformatics_analyst`: execution-focused computational subagent
- `senior_scientist`: literature and biological interpretation subagent

## How This Project Is Set Up

This project uses the main Codex thread as the Lead Researcher and keeps the focused specialists as subagents under `.codex/agents/`.

Main-thread instructions:

- The Lead Researcher behavior is defined in `AGENTS.md`.
- The root `AGENTS.md` is the canonical instruction file for the main session.

Subagent notes:

- `bioinformatics_analyst` is the execution specialist for computational work.
- `senior_scientist` is the interpretation specialist for literature context and biological plausibility.
- In this skeleton, `bioinformatics_analyst` has `workspace-write` access.
- `senior_scientist` is configured as `read-only`.

## Repository structure

- `README.md`: project overview and usage model
- `AGENTS.md`: main-thread operating instructions for the Lead Researcher
- `.codex/agents/bioinformatics_analyst.toml`: subagent config for computational execution
- `.codex/agents/senior_scientist.toml`: subagent config for scientific interpretation
- `lab_notebook.md`: running project record, created as the work begins
- `lab_notebook_figures/`: figures referenced from the notebook

## Working model

1. Define the biological question, available datasets, and the immediate decision to inform.
2. Use the Lead Researcher to choose the smallest decisive next analysis.
3. Delegate computational work to `bioinformatics_analyst`.
4. Use `senior_scientist` to interpret important findings in the context of prior literature.
5. Record results, decisions, and artifact paths in `lab_notebook.md`.

## Typical prompt

```text
Plan the next analysis steps for this project. Use bioinformatics_analyst to execute the top-priority computational analysis, then ask senior_scientist to interpret the result in the context of published literature.
```

## Notes

- This skeleton is meant to be adapted per project by adding data locations, analysis scripts, result directories, and a maintained lab notebook.
