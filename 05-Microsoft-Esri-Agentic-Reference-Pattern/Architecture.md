# Microsoft + Esri Agentic Reference Pattern Architecture

## Purpose

This document defines a conceptual architecture boundary for agentic reasoning grounded in Microsoft and Esri context.

## Architectural Position

The library narrative culminates in:

```text
Data → Spatial Processing → Spatial Experience → Context → Agentic Reasoning
```

This progression is conceptual. It does not assert a complete supported product integration.

## Candidate Architecture Layers

| Layer | Candidate responsibility | Status |
|---|---|---|
| Human experience | Ask, review, approve, reject, or escalate | VALIDATION REQUIRED |
| Microsoft Foundry | Agent orchestration, model access, evaluation, and tool use | SOURCE REQUIRED |
| Microsoft IQ / Fabric IQ | Business entities, relationships, and context | Depends on 04 validation |
| Fabric Data Agents | Supported access to Fabric data and semantic context | SOURCE REQUIRED |
| Semantic models | Governed business measures and analytical meaning | SOURCE REQUIRED |
| ArcGIS MCP | Supported spatial tools exposed to agents | SOURCE REQUIRED |
| Esri context | Authoritative spatial and domain information | VALIDATION REQUIRED |
| Ground Truth | Conceptual grounding across authoritative context | CONCEPTUAL PATTERN |
| Governance | Identity, authorization, audit, evaluation, and policy | VALIDATION REQUIRED |

## Candidate Interaction

```text
Human request
    → Agent orchestration
    → Authorized context retrieval
    → Optional spatial tool invocation
    → Grounded response or proposed action
    → Human review when required
    → Audited outcome
```

The sequence identifies validation points. It is not a supported protocol or product flow.

## Trust Boundaries to Validate

1. User to agent experience
2. Agent to Microsoft data and context
3. Agent to Data Agent
4. Agent to ArcGIS MCP
5. ArcGIS MCP to ArcGIS services or customer systems
6. Proposed action to human approval
7. Approved action to the target system
8. Logs, traces, evaluation data, and telemetry

## Architecture Questions

1. Which component authenticates the user and preserves identity?
2. Which component authorizes each data query and tool call?
3. Where are orchestration state, prompts, responses, and traces stored?
4. Which tools are read-only and which can change state?
5. How are tool schemas discovered and versioned?
6. How are spatial reference, scale, precision, and temporal context preserved?
7. How are conflicting sources and stale data handled?
8. Which actions require approval, and where is that policy enforced?
9. How are groundedness, correctness, and safety evaluated?

## Prohibited Assumptions

This pattern must not assume:

- Ground Truth is a Microsoft or Esri product.
- ArcGIS MCP is available with a particular tool set, identity model, or deployment pattern.
- Fabric IQ contains Esri domain models.
- A Data Agent can invoke ArcGIS MCP.
- Foundry automatically propagates end-user authorization to every tool.
- Agent outputs are authoritative without source attribution and validation.
- Consequential actions may run without scenario-appropriate approval.

## Validation Status

Conceptual Only
