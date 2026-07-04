# AI Agent Reliable Auditor

AI Agent Reliable Auditor is an orchestrated assurance system for evaluating whether an organizational AI agent remains operationally ready for use.

The system is designed for democratized AI agent creation, where non-engineering organizational users can create useful agents, but cannot be expected to maintain them with full DevOps, MLOps, or AgentOps practices.

The auditor does not attempt to prove that an open-ended AI agent is always semantically correct. Instead, it collects evidence about operational readiness, classifies risks, identifies unknowns, and produces practical remediation guidance.

## Core principle

The system separates task-level knowledge from reliability engineering.

Agent creators describe the intended task, expected behavior, required sources, tools, outputs, and examples of successful operation. The auditor system translates that information into reliability checks, readiness contracts, diagnostics, escalation guidance, and lifecycle controls.

## Agent architecture

The system is organized as an orchestrator and a set of focused auditor agents.

1. `00_orchestrator.md` - AI Agent Reliable Auditor
2. `01_evidence_intake_agent.md` - Evidence Intake Agent
3. `02_dependency_mapper_agent.md` - Dependency Mapper Agent
4. `03_model_dependency_auditor.md` - Model Dependency Auditor
5. `04_retrieval_source_auditor.md` - Retrieval Source Auditor
6. `05_tool_api_auditor.md` - Tool and API Auditor
7. `06_permission_credential_auditor.md` - Permission and Credential Auditor
8. `07_output_contract_auditor.md` - Output Contract Auditor
9. `08_workflow_scheduling_auditor.md` - Workflow and Scheduling Auditor
10. `09_semantic_degradation_auditor.md` - Semantic Degradation Auditor
11. `10_ownership_governance_auditor.md` - Ownership and Governance Auditor
12. `11_report_synthesis_agent.md` - Report Synthesis Agent
13. `12_readiness_contract_template.md` - Readiness Contract Template

## Evidence discipline

Every agent must separate:

- Confirmed findings
- Reproducible risks
- Unknowns
- Not-applicable checks

The auditor must never claim access to private settings, hidden dependencies, permissions, retrieval indexes, logs, or platform configuration unless explicit evidence is provided.

## Standard readiness status

Each sub-agent should return one of the following statuses:

- `READY`
- `NOT_READY`
- `READINESS_UNKNOWN`
- `NOT_EXTERNALLY_VERIFIABLE`
- `NOT_APPLICABLE`

## Intended use

This repository is intended to support transparent documentation of the prototype auditor, its sub-agent responsibilities, readiness-check logic, and expected outputs.
