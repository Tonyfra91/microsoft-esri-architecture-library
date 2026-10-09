# Fabric IQ + Spatial Intelligence

> **Library:** [Microsoft + Esri Architecture Library](../README.md) · Previous: [03 · ArcGIS Maps for Microsoft Fabric](../03-ArcGIS-Maps-for-Fabric/) · Next: [05 · Microsoft + Esri Agentic Reference Pattern](../05-Microsoft-Esri-Agentic-Reference-Pattern/)

## Executive Summary

This area explores how spatial and Esri domain context could participate in Microsoft IQ and Fabric IQ. It is a validation workspace, not a published product integration architecture.

> **VALIDATION REQUIRED**
>
> This library does not claim that Esri currently provides Fabric IQ ontologies, that Esri domain models have been mapped into Fabric IQ, or that a supported product integration exists.

## Microsoft IQ

Microsoft IQ provides the broader context for grounding analytics and agent experiences across organizational data and knowledge.

> **SOURCE REQUIRED**
>
> Collect authoritative Microsoft documentation that defines Microsoft IQ, its layers, product boundaries, and the relationship among Fabric IQ, Foundry IQ, Work IQ, and other named experiences.

## Fabric IQ

Fabric IQ is the focus of this exploration because it introduces business context that may include entities, relationships, semantic meaning, and data-driven experiences.

> **VALIDATION REQUIRED**
>
> Confirm the current Fabric IQ architecture, supported artifacts, lifecycle, APIs, governance model, and supported agent integrations.

## Ontology

The working question is whether validated Esri domain concepts and spatial relationships could be represented in, referenced by, or aligned with Fabric IQ ontology capabilities.

No ontology mapping is proposed in this version.

## Semantic Models

Semantic models may provide business measures and analytical context relevant to spatial scenarios.

> **SOURCE REQUIRED**
>
> Confirm the supported relationship between Fabric IQ ontology artifacts, Power BI semantic models, and other Fabric data items before drawing connections.

## Graph

Graph structures may be relevant where domain entities and spatial or network relationships must be traversed.

> **VALIDATION REQUIRED**
>
> Identify the graph capabilities intended by current Fabric IQ documentation and distinguish them from ArcGIS Knowledge, network datasets, and Utility Network topology.

## Data Agents

Data Agents may provide a conversational path to grounded enterprise data.

> **VALIDATION REQUIRED**
>
> Confirm supported data sources, semantic grounding, identity propagation, tool boundaries, and whether any spatial context can be represented or invoked.

## Esri Spatial Context

Candidate spatial context includes location, geometry, containment, adjacency, proximity, routing, network connectivity, service territory, and other geographic relationships.

These examples are discovery categories, not Fabric IQ integration claims.

## Domain Grounding

Domain grounding requires authoritative definitions of entities, properties, relationships, rules, hierarchies, and spatial meaning.

The first candidate domain is Esri Utility Network. See [Esri Domain Model Validation](Esri-Domain-Model-Validation.md).

## Open Engineering Questions

The central engineering question is:

> **ENGINEERING QUESTION**
>
> For Utility Network and other Esri domains, where is the authoritative domain model encoded today? Does Esri have information models, schemas, knowledge graph models, formal ontologies, or some combination, and are those definitions and relationships available in a machine-readable form?

Additional questions:

1. Which definitions are product behavior, implementation templates, industry models, or customer configuration?
2. Which artifacts are authoritative and versioned?
3. Which relationships are semantic, topological, spatial, operational, or inferred?
4. Which artifacts may be exported, queried, or consumed programmatically?
5. Which concepts could be candidates for Fabric IQ mapping without losing Esri semantics?

## Validation Plan

1. Collect authoritative Microsoft IQ and Fabric IQ documentation.
2. Collect Esri Utility Network domain artifacts.
3. Classify the Esri artifacts by model type and authority.
4. Confirm machine-readable availability and licensing constraints.
5. Review findings with Microsoft and Esri engineering.
6. Define candidate mappings only after both source models are understood.
7. Test mappings in a bounded scenario before publishing architecture.

## Sources and Evidence

| Document | Purpose |
|---|---|
| [Architecture](Architecture.md) | Exploration boundary and candidate architecture questions |
| [Architecture Mapping](Architecture-Mapping.md) | Validation gates for each proposed architecture layer |
| [Esri Domain Model Validation](Esri-Domain-Model-Validation.md) | Utility Network-first engineering discovery framework |
| [Evidence register](records/Evidence.md) | Candidate claims awaiting authoritative support |
| [Source register](records/Source-Register.md) | Microsoft and Esri sources to collect and review |
| [Collection checklist](records/Collection-Checklist.md) | Required artifacts and engineering confirmations |

## Architecture Status

Exploration and Validation
