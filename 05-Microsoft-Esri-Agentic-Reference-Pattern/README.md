# Microsoft + Esri Agentic Reference Pattern

> **Library:** [Microsoft + Esri Architecture Library](../README.md) · Previous: [04 · Fabric IQ + Spatial Intelligence](../04-Fabric-IQ-Spatial-Intelligence/)

## Executive Summary

This area explores how Microsoft Foundry, Microsoft IQ and Fabric IQ context, Fabric Data Agents, ArcGIS MCP, and other tools could participate in a governed agentic pattern grounded in enterprise and spatial context.

It is a conceptual reference pattern. It does not claim that a complete Microsoft + Esri production architecture currently exists.

## Microsoft Foundry

Microsoft Foundry is a candidate platform for agent orchestration, model access, evaluation, and tool integration.

> **SOURCE REQUIRED**
>
> Collect current Foundry agent architecture, identity, tool, networking, evaluation, and governance documentation before assigning components or flows.

## Microsoft IQ / Fabric IQ Context

Validated Microsoft IQ and Fabric IQ context could provide business meaning for agent reasoning.

> **VALIDATION REQUIRED**
>
> This pattern depends on the findings from [04 · Fabric IQ + Spatial Intelligence](../04-Fabric-IQ-Spatial-Intelligence/). No Esri-to-Fabric-IQ mapping is assumed.

## Fabric Data Agents

Fabric Data Agents are a candidate route to supported Fabric data and semantic context.

> **VALIDATION REQUIRED**
>
> Confirm supported data sources, agent-to-agent or tool integration, identity propagation, authorization, and response-grounding behavior.

## Semantic Models

Semantic models may provide governed business measures and analytical definitions.

> **SOURCE REQUIRED**
>
> Confirm how a Foundry agent or Data Agent may access semantic models and how authorization is enforced for each request.

## Ontology

Ontology may provide entities and relationships for grounded reasoning.

This pattern does not assume an Esri ontology or a completed mapping to Fabric IQ.

## ArcGIS MCP

ArcGIS MCP is treated as a candidate agent tool boundary.

> **SOURCE REQUIRED**
>
> Collect authoritative ArcGIS MCP documentation, supported tools, transport, hosting, identity, authorization, data handling, deployment, and lifecycle information.

## Agent Tools and Actions

Potential tools may retrieve context, answer spatial questions, or propose actions. No tool inventory or write capability is asserted.

> **VALIDATION REQUIRED**
>
> Each tool requires an explicit contract, allowed operations, input validation, identity context, audit behavior, failure handling, and human-approval policy.

## Esri Spatial and Domain Context

Candidate context includes authoritative ArcGIS content, spatial relationships, domain models, network state, and analytical results.

The authority, freshness, lineage, and machine-readable representation of each context source must be validated.

## Ground Truth

[Ground Truth](Ground-Truth.md) is a conceptual pattern for combining authoritative business, spatial, domain, and operational context so an agent can produce grounded answers or proposed actions.

Ground Truth is not an existing Microsoft or Esri product.

## Human Interaction and Agent Experience

The intended experience keeps people accountable for consequential decisions. Human review, approval, override, and escalation requirements must be designed per scenario.

## Identity, Security, and Governance Validation

The pattern is incomplete until it documents:

- End-user and workload identities
- Authorization at each data and tool boundary
- Credential and token handling
- Tenant and network boundaries
- Data residency and telemetry
- Prompt, response, and tool-call logging
- Human approval and separation of duties
- Audit, evaluation, monitoring, and incident response

## Open Engineering Questions

1. Which Microsoft agent component owns orchestration?
2. Which context is supplied by Fabric IQ, a Data Agent, semantic models, or direct tools?
3. What is ArcGIS MCP's supported deployment and identity model?
4. Which spatial operations are read-only, analytical, or mutating?
5. How is user authorization preserved across agent and tool calls?
6. How are source authority, freshness, and lineage represented?
7. Which actions require human approval?
8. How are grounding quality and spatial correctness evaluated?
9. How does the pattern fail safely when data or tools are unavailable?

## Supporting Technical Records

| Document | Purpose |
|---|---|
| [Architecture](Architecture.md) | Conceptual layers, boundaries, and validation gates |
| [Architecture Mapping](Architecture-Mapping.md) | Evidence needed for each proposed interaction |
| [Ground Truth](Ground-Truth.md) | Definition and validation framework for the conceptual pattern |
| [Evidence register](records/Evidence.md) | Candidate claims awaiting support |
| [Source register](records/Source-Register.md) | Authoritative sources to collect |
| [Collection checklist](records/Collection-Checklist.md) | Required artifacts and engineering validation |

## Architecture Status

Conceptual Reference Pattern
