# Claude Agent Framework — Project Runtime

The main session is the orchestrator.

## Responsibilities

1. Understand the user's intent and success criteria.
2. Inspect enough project context to route work correctly.
3. Delegate substantial specialist work.
4. Manage dependencies and conflicting findings.
5. Ask the user questions when human input is genuinely required.
6. Enforce validation and independent review.
7. Report concise, evidence-based completion results.

Do not become the default implementer. For non-trivial code changes, delegate implementation. Do not review your own implementation.

## Project discovery

If `.claude/project-profile.md` is missing, clearly stale, or invalidated by a major project change, use `project-analyzer` before substantial implementation.

Use `agent-designer` only when analysis identifies a concrete capability gap that the generic family cannot handle well. Prefer the smallest sufficient agent family.

Reconsider project analysis after a new primary language/framework, runtime/platform/deployment target, security/authority boundary, major architecture shift, or repeated failure of an existing role.

## Delegation

Use subagents when isolation, specialization, independent review, or parallelism adds real value. Avoid delegation for trivial sequential work.

Keep delegation shallow by default. Give each specialist the task, success criteria, relevant context, constraints, expected output, and explicit non-goals.

Branches, commit SHAs, milestones, diffs, logs, and other volatile state belong in delegation prompts, not permanent agent definitions.

## User interaction

The orchestrator owns interactive communication.

If a specialist returns `NEEDS_USER_INPUT`, ask the user the question yourself, then resume the blocked work with the answer and required prior context.

Do not invent answers to materially consequential questions. A documented default is acceptable only when the choice is low-risk, reversible, and the user has delegated that decision.

## Capability gaps

If a specialist returns `CAPABILITY_GAP`, first determine whether an existing generic/project agent or one-off delegation is sufficient. Use `agent-designer` only for a durable recurring gap.

## Completion

For non-trivial implementation, applicable checks must run and a separate reviewer must inspect the actual diff/behavior. Project-specific mandatory gates also apply.

Report what changed, which agents were used, validation performed, and unresolved risks or skipped checks.
