# ArcGIS Maps for Microsoft Fabric

> **Library:** [Microsoft + Esri Architecture Library](../README.md) · Previous: [02 · ArcGIS GeoAnalytics for Microsoft Fabric](../02-GeoAnalytics-for-Fabric/) · Next: [04 · Fabric IQ + Spatial Intelligence](../04-Fabric-IQ-Spatial-Intelligence/)

## Executive Summary

ArcGIS Maps for Microsoft Fabric provides mapping, visualization, exploration, and location-aware experiences within Microsoft Fabric. This component establishes the collection and validation framework needed to document the product architecture without inferring unsupported integrations or dependencies.

> **VALIDATION REQUIRED**
>
> Product capabilities, supported inputs, setup requirements, identity behavior, data movement, limitations, and deployment boundaries must be traced to current Microsoft and Esri documentation before this component is presented as a validated architecture.

## Where ArcGIS Maps for Microsoft Fabric Fits

This component follows [ArcGIS GeoAnalytics for Microsoft Fabric](../02-GeoAnalytics-for-Fabric/) in the library progression:

```text
Data → Spatial Processing → Spatial Experience
```

GeoAnalytics and Maps for Fabric are related but not interchangeable. GeoAnalytics provides distributed spatial processing in Fabric Spark. Maps for Fabric provides an experience for mapping and exploring supported data in Fabric.

## Architecture

See [Architecture](Architecture.md) for the architecture boundary, candidate questions, and validation status.

> **VALIDATION REQUIRED**
>
> Collect authoritative evidence for the product boundary, Fabric workload components, ArcGIS services, administrative controls, and any external service communication before drawing a deployment architecture.

## Data Flow

No end-to-end data flow is asserted yet.

> **VALIDATION REQUIRED**
>
> Confirm supported data sources, whether data is copied or queried, how OneLake data is accessed, refresh behavior, output behavior, and any network boundary crossings.

## Identity / Authentication

No identity or authentication flow is asserted yet.

> **VALIDATION REQUIRED**
>
> Confirm Fabric identity requirements, ArcGIS identity requirements, anonymous or signed-in behavior, licensing, token handling, tenant controls, and authorization boundaries.

## Dependencies

The dependency list remains open until current product documentation is reviewed.

> **VALIDATION REQUIRED**
>
> Confirm required Fabric capacity, workspace, workload installation or enablement, tenant settings, ArcGIS organization requirements, browser requirements, and supported regions.

## Scope and Boundaries

This area covers current, documented ArcGIS Maps for Microsoft Fabric behavior. It does not claim that:

- Every Fabric data item can be mapped.
- Every ArcGIS layer or service type is supported.
- GeoAnalytics is required to use Maps for Fabric.
- Data moves between Fabric and ArcGIS without an explicit documented path.
- ArcGIS for Power BI and ArcGIS Maps for Microsoft Fabric are interchangeable.
- Identity, networking, or governance behavior matches another ArcGIS integration.

## Customer Scenario

A customer scenario will be added after the supported data path and product prerequisites are validated.

> **VALIDATION REQUIRED**
>
> Select one bounded scenario with a measurable business question, supported Fabric data, a documented map workflow, an identified audience, and explicit success criteria.

## Minimum POC Pattern

A minimum proof-of-concept pattern will be documented only after the required components and supported flow are evidenced.

Initial discovery should identify:

1. The business question that requires a map.
2. The authoritative Fabric data item.
3. The location fields or geometry available.
4. The supported ArcGIS Maps for Fabric workflow.
5. The intended audience and access model.
6. The measurable validation outcome.

## Supporting Technical Records

| Document | Purpose |
|---|---|
| [Customer Guidance](01-Customer-Guidance.md) | Discovery questions, proof-of-concept framing, and validation boundaries |
| [Architecture](Architecture.md) | Candidate component architecture and open architecture questions |
| [Architecture Mapping](Architecture-Mapping.md) | Required architecture views and their evidence gates |
| [Evidence register](records/Evidence.md) | Candidate claims awaiting validation and supported claims once established |
| [Source register](records/Source-Register.md) | Authoritative sources reviewed for this component |
| [Collection checklist](records/Collection-Checklist.md) | Artifacts and evidence still required |

## Architecture Status

Validation Framework
