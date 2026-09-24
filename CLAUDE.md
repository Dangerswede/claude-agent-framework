# Framework Development Instructions

This repository develops a reusable Claude Code agent framework.

Do not add project-specific assumptions to the generic framework. A behavior belongs here only when broadly reusable across unrelated projects.

Keep the main orchestrator thin. Prefer specialist delegation for substantial implementation, deep analysis, testing, and review. Preserve one user-interaction boundary through the orchestrator.

Before changing framework behavior, read the relevant files in `docs/` and `framework/protocols/`.

Treat MeldOS and other repositories only as test cases and sources of lessons, never as generic project rules.
