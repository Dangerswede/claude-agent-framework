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

## Discovery is broader than stack detection

New projects are profiled before durable specialists are created. Discovery must identify not only languages and frameworks but also architecture invariants, domain/business rules, authoritative documentation, external source material, human-owned decisions, and places where correctness depends on interpretation.

A project whose difficult part is domain logic should not automatically receive more technology agents. The framework should prefer a narrow domain specialist when that closes the real recurring capability gap.

## Authority boundary

Agents may implement documented policy, but they must not silently invent unresolved domain policy.

Questions owned by a user, domain expert, customer, regulator, or other authority flow through NEEDS_USER_INPUT to the orchestrator.

The project profile records which sources are authoritative and which decisions require human authority.

## Specialization

Agent-designer creates only narrow project-owned agents justified by documented recurring capability gaps. Technology presence alone is not justification for a specialist.

Generic framework files should remain stable. Project-specific specialists, policies, and profiles belong to the consuming repository.

Delegation is shallow by default. Independent review remains separate from implementation.
