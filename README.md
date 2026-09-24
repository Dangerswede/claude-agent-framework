# Claude Agent Framework

Reusable Claude Code framework for orchestrator-first development.

The main Claude session acts primarily as a coordinator: understand intent, discover the project's needs, delegate substantial work, manage dependencies, ask the user questions, and enforce validation. Project-specific specialists are discovered from the repository instead of copied from another project.

## v0.1 principles

- One human interface: the orchestrator owns user interaction.
- Discover before specializing: analyze a project before creating project-specific agents.
- Small stable core: generic agents remain reusable and cache-friendly.
- Project-owned specialization: generated specialists live with the project.
- No agent explosion: create a specialist only for a concrete, recurring capability gap.
- Independent review: non-trivial implementation is reviewed by an agent that did not implement it.
- Stable context first: keep framework/project instructions stable and volatile task state in delegation prompts.

## Core family

`orchestrator`, `project-analyzer`, `agent-designer`, `planner`, `researcher`, `implementer`, `tester`, `reviewer`.

## Repository layout

- `framework/` — framework-owned runtime payload.
- `templates/` — project-owned files created during bootstrap/discovery.
- `docs/` — architecture, lifecycle, caching, model, and bootstrap decisions.
- `CLAUDE.md` — instructions for developing this framework itself, not a file to copy blindly into consuming projects.

## Bootstrap

Start with `docs/bootstrap.md`. v0.1 intentionally uses a documented, non-destructive bootstrap rather than an installer that might overwrite an existing project's Claude configuration. Automation can be added after this ownership contract has been integration-tested.

## Model policy

v0.1 targets Claude Opus 5.5 for orchestration and high-risk framework reasoning, Claude Sonnet 5 for normal engineering roles, and Haiku 4.5 for lightweight research. Exact choices are documented in `docs/model-selection.md`.

MeldOS may be used as a test project, but it is not the template for this framework.
