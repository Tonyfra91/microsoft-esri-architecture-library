# Fabric IQ + Spatial Intelligence

> **Library:** [Microsoft + Esri Architecture Library](../README.md) · Previous: [03 · ArcGIS Maps for Microsoft Fabric](../03-ArcGIS-Maps-for-Fabric/) · Next: [05 · Microsoft + Esri Agentic Reference Pattern](../05-Microsoft-Esri-Agentic-Reference-Pattern/)

## Executive Summary

This component provides a bounded preview pattern for representing business entities and precomputed spatial relationships in Fabric IQ ontology. It builds on governed OneLake data, spatial processing from ArcGIS GeoAnalytics for Microsoft Fabric, and the same supported data that may be visualized in ArcGIS Maps for Microsoft Fabric.

The minimum pattern does not claim a native Esri-to-Fabric-IQ integration. GeoAnalytics computes required spatial relationships, Fabric data engineering persists them, ontology binds the resulting entities and relationships, and ArcGIS Maps can visualize the same governed data through its independently supported source path.

> [!IMPORTANT]
> Ontology and several related capabilities are in preview. Use this pattern for a bounded proof of concept and validate current tenant settings, availability, lifecycle, limits, and support before production use.

## Minimum Scenario

The reference question is:

> Which operational assets are located within high-risk service areas, have open work orders, and are associated with recent incidents?

The MVP uses five entity types:

- Asset
- Work order
- Incident
- Service area
- Risk area

GeoAnalytics prepares spatial relationships such as **Asset within Service Area** and **Asset within Risk Area** before the ontology binds them.

## End-to-End Pattern

```text
Authoritative business and ArcGIS data
    → GeoAnalytics computes required spatial relationships
    → Governed entity and relationship tables are saved in OneLake
    → Fabric IQ ontology binds business meaning to the data
    → People explore relationships and validate ontology-agent answers
    → ArcGIS Maps may visualize the same governed source data
```

## Start Here

| Need | Page |
|---|---|
| Understand fit, requirements, and scope | [Customer Guidance](01-Customer-Guidance.md) |
| Follow the complete MVP | [End-to-End Scenario](02-End-to-End-Scenario.md) |
| Establish tenant and workspace readiness | [Stage 1: Establish the Foundation](03-Stage-1-Establish-the-Foundation.md) |
| Prepare entities and spatial relationships | [Stage 2: Prepare Entities and Relationships](04-Stage-2-Prepare-Entities-and-Relationships.md) |
| Create and bind the ontology | [Stage 3: Build and Bind the Ontology](05-Stage-3-Build-and-Bind-the-Ontology.md) |
| Explore, validate, and decide | [Stage 4: Explore and Validate](06-Stage-4-Explore-and-Validate.md) |
| Review architecture boundaries | [Architecture](Architecture.md) |

## Advanced Research Track

[Esri Domain Model Validation](Esri-Domain-Model-Validation.md) remains an advanced research track for Utility Network and other Esri domain models. It is not a prerequisite for the MVP.

## Supporting Technical Records

| Document | Purpose |
|---|---|
| [Architecture Mapping](Architecture-Mapping.md) | Architecture views and evidence status |
| [Evidence register](records/Evidence.md) | Claims mapped to authoritative sources and open gaps |
| [Source register](records/Source-Register.md) | Microsoft sources and unresolved Esri sources |
| [Collection checklist](records/Collection-Checklist.md) | Remaining collection and engineering work |

## Architecture Status

Evidence-Backed Preview Pattern with Open Esri Integration Questions
