# Framework Ownership Contract

Files in this directory are source templates for framework-owned behavior.

A consuming repository owns its project profile, project-specific agents, local architecture/security rules, and task state.

Framework updates must never silently replace project-owned content.

Dynamic values such as current branch, commit, PR, milestone, date, diff, logs, and task identifiers are task context and must not be persisted into generic agent definitions.
