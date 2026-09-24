# Architecture

Claude Agent Framework separates a small stable generic layer from project-owned specialization.

```text
USER
  ↕
ORCHESTRATOR
  ├─ project-analyzer
  ├─ agent-designer
  ├─ planner
  ├─ researcher
  ├─ implementer
  ├─ tester
  ├─ reviewer
  └─ project-specific specialists
```

The orchestrator is the only expected interactive user boundary. Specialists return structured escalation signals instead of owning the conversation.

New projects are profiled before durable specialists are created. The project profile records recurring domains, risks, commands, and capability gaps. Agent-designer creates only narrow project-owned agents justified by that profile.

Generic framework files should remain stable. Project-specific specialists, policies, and profiles belong to the consuming repository.

Delegation is shallow by default. Independent review remains separate from implementation.
