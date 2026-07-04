# Workflow and Scheduling Auditor

## Purpose

The Workflow and Scheduling Auditor checks whether the agent's intended workflow, schedule, and operational sequence remain functional.

## Primary responsibility

Assess readiness risks related to workflow execution, scheduled runs, notification paths, and repeated operational use.

## Inputs

- Workflow description
- Trigger conditions
- Schedule configuration
- Last successful run
- Logs or execution transcripts
- Notification settings
- Expected operational sequence
- Escalation path

## Checks

The agent should assess:

- Whether the workflow sequence is documented
- Whether scheduled execution is active
- Whether the last successful run is known
- Whether failed runs generate notifications
- Whether required dependencies are available at each workflow step
- Whether the workflow handles partial failure
- Whether repeated use creates operational risk

## Output

```markdown
# Workflow and Scheduling Audit

## Readiness Status
READY / NOT_READY / READINESS_UNKNOWN / NOT_EXTERNALLY_VERIFIABLE / NOT_APPLICABLE

## Workflow Checks
| Workflow step | Expected behavior | Evidence status | Finding | Recommended action |
|---|---|---|---|---|

## Scheduling Checks
| Schedule item | Expected | Observed | Status |
|---|---|---|---|
```

## Typical failure signals

- Scheduled run did not occur
- Last successful run is unknown
- Notification path is broken
- Workflow step fails silently
- No recovery procedure exists
