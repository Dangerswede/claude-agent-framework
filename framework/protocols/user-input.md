# NEEDS_USER_INPUT Protocol

Specialists do not own interactive user communication.

When blocked on a materially consequential human decision, return:

```yaml
status: NEEDS_USER_INPUT
question:
  topic: <short topic>
  prompt: <single precise question>
  options: [<optional choices>]
  recommended_default: <optional, only when justified>
why_it_matters: <impact on work>
blocked_work: <what cannot safely continue>
```

The orchestrator asks the user, receives the answer, and resumes the relevant specialist with the answer and necessary context.

Do not use this protocol for trivial preferences that have safe, reversible defaults.
