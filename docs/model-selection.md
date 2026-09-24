# Model Selection Policy

Framework v0.1 uses explicit Claude Code model IDs.

| Role class | Default model | Typical effort |
|---|---|---|
| Orchestration / agent design / project discovery | `claude-opus-5-5` | high |
| General planning / implementation / testing / review | `claude-sonnet-5` | high |
| Lightweight current research | `claude-haiku-4-5-20251001` | medium |
| Exceptional project specialist | choose deliberately | high/xhigh |

Claude Opus 5.5 is the baseline high-capability model for this framework.

Do not duplicate model-selection prose inside every project-specific prompt. Use the narrowest sufficient model for the role, but never silently downgrade a role where the project requires a stronger model.

When Anthropic releases or retires models, update this policy and framework-owned agent definitions together. Project-owned specialist agents should be reviewed separately rather than overwritten blindly.
