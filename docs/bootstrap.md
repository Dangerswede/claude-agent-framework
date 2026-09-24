# Safe Bootstrap

The framework must be adoptable by a new repository without destroying existing Claude Code configuration.

## Ownership model

Framework-owned:
- the generic agent definitions shipped under `framework/.claude/agents/`;
- generic runtime behavior from `framework/CLAUDE.md`;
- generic protocols.

Project-owned:
- project-specific instructions and architecture/security rules;
- `.claude/project-profile.md`;
- project-specific specialist agents;
- existing Claude Code settings unrelated to this framework.

## New project

1. Copy the generic agent definitions into `.claude/agents/`.
2. Merge the settings keys from `framework/.claude/settings.json` into the project's settings rather than replacing unrelated settings.
3. Incorporate the runtime rules from `framework/CLAUDE.md` into the project's Claude instructions.
4. Create `.claude/project-profile.md` from `templates/project-profile.md`.
5. Run project-analyzer.
6. Let agent-designer create only durable specialists justified by documented capability gaps.
7. Commit the resulting project-owned profile and specialist definitions with the project.

## Existing project

Never overwrite `CLAUDE.md`, `.claude/settings.json`, or unknown agents wholesale.

First inspect existing instructions and agents. Merge generic orchestration behavior with the project's authoritative rules. Name conflicts must be resolved explicitly.

Project-specific rules win over generic framework defaults when they intentionally constrain the project, unless doing so would violate a higher-level safety or platform requirement.

## Updates

Framework updates may replace framework-owned generic agent definitions only after reviewing local modifications.

They must not overwrite:
- project-profile;
- generated project specialists;
- project-specific Claude instructions;
- unrelated settings.

v0.1 does not automate updates until this ownership boundary has been tested on real repositories.
