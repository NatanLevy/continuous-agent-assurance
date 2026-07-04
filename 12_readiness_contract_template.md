# Readiness Contract Template

## Purpose

A readiness contract defines the minimum observable conditions under which an AI agent should be treated as operationally ready.

It does not prove that every future answer will be correct. It defines repeatable checks that can detect operational failure or degradation early.

## Agent identity

- Agent name:
- Owner:
- Maintainer:
- Business unit:
- Intended users:
- Criticality level:
- Intended workflow:
- Escalation path:

## Declared dependencies

| Dependency type | Dependency | Required? | Owner | Verification method |
|---|---|---|---|---|
| Model |  |  |  |  |
| Source |  |  |  |  |
| Tool/API |  |  |  |  |
| Permission |  |  |  |  |
| Workflow |  |  |  |  |
| Output format |  |  |  |  |

## Minimum readiness conditions

| Condition | Check method | Expected result | Evidence required | Failure response |
|---|---|---|---|---|
| Required sources are reachable |  |  |  |  |
| Representative queries return expected material |  |  |  |  |
| Required tools execute successfully |  |  |  |  |
| Output satisfies mandatory structure |  |  |  |  |
| Owner and escalation path are valid |  |  |  |  |
| Representative prompts satisfy task-level expectations |  |  |  |  |

## Readiness status

- READY:
- NOT_READY:
- READINESS_UNKNOWN:
- NOT_EXTERNALLY_VERIFIABLE:
- NOT_APPLICABLE:

## Remediation rules

If a critical check fails:

1. Mark the agent as not ready.
2. Identify the dependency affected.
3. Notify the owner or administrator.
4. Recommend a specific remediation action.
5. Record the evidence and timestamp.
6. Re-run the readiness check after remediation.

## Review cadence

- Low-criticality agent:
- Recurring operational workflow:
- Customer-facing workflow:
- Engineering, legal, financial, or regulated workflow:
