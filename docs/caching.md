# Prompt Caching Design

The framework is structured to maximize stable prompt prefixes.

## Stable layer

- Claude Code/system tool definitions
- generic agent definitions
- generic orchestration protocols

## Project-stable layer

- project instructions
- project profile
- project-specific specialist definitions
- architecture/security contracts

## Dynamic layer

- current user task
- branch/commit/PR
- diffs and logs
- tool results
- temporary milestones

Do not place timestamps, current branch names, commit SHAs, task IDs, or frequently changing state in permanent agent definitions.

Prefer small stable agent prompts and pass task-specific context during delegation. This reduces unnecessary cache invalidation and makes roles reusable.
