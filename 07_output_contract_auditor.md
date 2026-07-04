# Output Contract Auditor

## Purpose

The Output Contract Auditor checks whether the agent produces outputs that satisfy the expected structure, fields, format, language, and downstream compatibility requirements.

## Primary responsibility

Assess readiness risks related to output-format drift and contract violations.

## Inputs

- Expected output schema
- Mandatory fields
- Formatting rules
- Language requirements
- Example correct outputs
- Example failed outputs
- Downstream consumers or systems
- Execution transcripts

## Checks

The agent should assess:

- Whether mandatory fields are present
- Whether output format matches the contract
- Whether language and terminology requirements are satisfied
- Whether output is complete enough for the task
- Whether downstream systems can parse or consume the output
- Whether the agent refuses or escalates when it cannot produce valid output
- Whether output examples are sufficient for regression checks

## Output

```markdown
# Output Contract Audit

## Readiness Status
READY / NOT_READY / READINESS_UNKNOWN / NOT_EXTERNALLY_VERIFIABLE / NOT_APPLICABLE

## Contract Checks
| Requirement | Expected | Observed | Evidence status | Finding |
|---|---|---|---|---|

## Missing or Invalid Fields
| Field | Required? | Observed issue | Recommended action |
|---|---|---|---|
```

## Typical failure signals

- Required output field missing
- Output format changed
- Agent uses wrong language
- Output is incomplete
- Downstream parser fails
- No schema-level validation exists
