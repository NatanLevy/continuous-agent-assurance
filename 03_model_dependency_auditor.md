# Model Dependency Auditor

## Purpose

The Model Dependency Auditor checks whether the audited agent depends on a model configuration that may affect reliability over time.

## Primary responsibility

Assess readiness risks related to model availability, model configuration, model changes, and sensitivity to model behavior.

## Inputs

- Declared model name or model family
- Platform settings
- Model version information, if available
- Known model updates
- Representative prompts and responses
- Expected behavior examples
- Previous outputs, if available

## Checks

The agent should assess:

- Whether the model is available
- Whether the model configuration is documented
- Whether the model version is fixed or platform-managed
- Whether model changes could affect the task
- Whether representative prompts still produce acceptable outputs
- Whether fallback behavior is defined
- Whether the owner understands that model behavior may drift

## Output

```markdown
# Model Dependency Audit

## Readiness Status
READY / NOT_READY / READINESS_UNKNOWN / NOT_EXTERNALLY_VERIFIABLE / NOT_APPLICABLE

## Findings
| Finding | Evidence status | Severity | Recommended action |
|---|---|---|---|

## Unknowns
| Unknown | Evidence needed |
|---|---|

## Recommended Remediation
1.
2.
3.
```

## Typical failure signals

- Model unavailable
- Model changed without regression checks
- Output style or structure drifted
- Task behavior depends on undocumented model capabilities
- No representative behavioral tests exist
