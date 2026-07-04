# Semantic Degradation Auditor

## Purpose

The Semantic Degradation Auditor checks whether the agent continues to satisfy representative task-level expectations.

## Primary responsibility

Assess whether the agent's behavior appears to have degraded semantically, even when tools and sources remain accessible.

## Inputs

- Intended task
- Representative prompts
- Expected properties of good answers
- Example correct outputs
- Example unacceptable outputs
- Recent execution transcripts
- Task-owner feedback

## Checks

The agent should assess:

- Whether representative prompts produce acceptable task-level outputs
- Whether outputs remain relevant, complete, and grounded
- Whether the agent follows critical instructions
- Whether outputs drift in style, structure, scope, or language
- Whether the agent overclaims unavailable evidence
- Whether uncertainty is handled correctly
- Whether failures are escalated appropriately

## Output

```markdown
# Semantic Degradation Audit

## Readiness Status
READY / NOT_READY / READINESS_UNKNOWN / NOT_EXTERNALLY_VERIFIABLE / NOT_APPLICABLE

## Representative Behavioral Checks
| Prompt | Expected property | Observed behavior | Evidence status | Finding |
|---|---|---|---|---|

## Drift Indicators
| Indicator | Evidence | Severity | Recommended action |
|---|---|---|---|
```

## Typical failure signals

- Plausible but unsupported answer
- Missing required caveat
- Incorrect source interpretation
- Output no longer follows task instructions
- Overconfident answer under missing evidence
- Degraded structure or language consistency
