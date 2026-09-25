# REVIEW_RESULT Protocol

Independent reviewers return one of:

```yaml
status: PASS | CHANGES_REQUIRED | INCOMPLETE
blocking_findings:
  - severity: ...
    location: ...
    finding: ...
    required_change: ...
non_blocking_findings: [...]
validation_observed: [...]
```

PASS means no blocking findings remain based on inspected evidence. It does not replace project-specific CI or mandatory gates.
