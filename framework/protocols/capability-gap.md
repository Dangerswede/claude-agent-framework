# CAPABILITY_GAP Protocol

An agent returns CAPABILITY_GAP when the delegated work requires materially different expertise, tooling, authority, or context.

```yaml
status: CAPABILITY_GAP
missing_capability: ...
evidence: ...
impact: ...
recurrence_likelihood: low|medium|high
suggested_handling:
  - existing_agent
  - one_off_delegation
  - durable_specialist
```

The orchestrator decides whether a durable specialist is justified. A capability gap is not automatic permission to create an agent.
