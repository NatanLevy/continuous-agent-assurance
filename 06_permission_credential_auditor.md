# Permission and Credential Auditor

## Purpose

The Permission and Credential Auditor checks whether the agent has the required access rights, credentials, tokens, and connector scopes to operate.

## Primary responsibility

Assess readiness risks related to authentication, authorization, expired tokens, user-specific permissions, and connector access.

## Inputs

- Declared permissions
- Connector list
- User roles or access scopes, if available
- Token or credential status, if available
- Access failure reports
- Execution logs
- Evidence of source access
- Evidence of tool access

## Checks

The agent should assess:

- Whether required permissions are documented
- Whether credentials or tokens remain valid
- Whether connector scopes are sufficient
- Whether access differs across users or roles
- Whether permissions expire or require renewal
- Whether the agent fails safely when access is denied
- Whether administrators have a renewal or escalation path

## Output

```markdown
# Permission and Credential Audit

## Readiness Status
READY / NOT_READY / READINESS_UNKNOWN / NOT_EXTERNALLY_VERIFIABLE / NOT_APPLICABLE

## Access Checks
| Resource | Required permission | Evidence status | Finding | Recommended action |
|---|---|---|---|---|

## Credential Risks
| Credential or connector | Risk | Evidence needed | Recommended action |
|---|---|---|---|
```

## Typical failure signals

- Permission expired
- Token invalid
- Connector disconnected
- User cannot access required source
- Access works for creator but not for shared users
- No owner knows how to renew access
