# Delegation Protocol

Permanent agent definitions stay stable; dynamic task context belongs in delegation prompts.

Recommended envelope:

```yaml
task:
  objective: ...
  success_criteria: [...]
scope:
  in: [...]
  out: [...]
context:
  relevant_files: [...]
  constraints: [...]
authority:
  may_modify: true|false
expected_output: ...
```

Delegate only the context required for the role. Avoid restating large stable project instructions already available to the agent.
