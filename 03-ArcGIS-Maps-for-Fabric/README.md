# ArcGIS Maps for Microsoft Fabric

> **Library:** [Microsoft + Esri Architecture Library](../README.md) · Previous: [02 · ArcGIS GeoAnalytics for Microsoft Fabric](../02-GeoAnalytics-for-Fabric/) · Next: [04 · Fabric IQ + Spatial Intelligence](../04-Fabric-IQ-Spatial-Intelligence/)

## Executive Summary

ArcGIS Maps for Microsoft Fabric is an Esri mapping workload for creating interactive, multiscale maps within Microsoft Fabric. A map author works from a Fabric workspace, signs in with an ArcGIS Online organizational account, and adds supported lakehouse, ArcGIS Online, or ArcGIS Living Atlas data.

This component provides an evidence-backed proof-of-concept path from tenant enablement through map validation. Production network, telemetry, data-residency, refresh, and sharing details still require customer-specific validation.

## Where ArcGIS Maps for Microsoft Fabric Fits

This component follows [ArcGIS GeoAnalytics for Microsoft Fabric](../02-GeoAnalytics-for-Fabric/) in the library progression:

```text
Data → Spatial Processing → Spatial Experience
```

GeoAnalytics and Maps for Fabric are related but not interchangeable. GeoAnalytics provides distributed spatial processing in Fabric Spark. Maps for Fabric provides an experience for mapping and exploring supported data in Fabric.

## Product Naming

ArcGIS Maps for Microsoft Fabric is also called **ArcGIS Maps for Fabric** in the product workflow. It must not be confused with:

- ArcGIS GeoAnalytics for Microsoft Fabric, the Spark spatial-processing library
- Fabric Maps or the Map item in Real-Time Intelligence, a Microsoft mapping experience based on Azure Maps
- ArcGIS for Power BI, the Power BI visual
- ArcGIS for Microsoft Fabric, Esri's umbrella offering

Use the [product-selection matrix](01-Customer-Guidance.md#choose-the-right-spatial-experience)
to compare ArcGIS Maps for Fabric with ArcGIS for Power BI. See
[Public Research](records/Public-Research.md#product-naming) for the evidence
boundary.

## Start Here

Read the documents in this order:

| Step | Document | What it covers |
|---|---|---|
| 1 | [Customer Guidance](01-Customer-Guidance.md) | Product fit, foundational requirements, discovery, and POC framework |
| 2 | [End-to-End Scenario](02-End-to-End-Scenario.md) | Four-stage implementation path |
| 3 | [Stage 1: Enable and Authorize](03-Stage-1-Enable-and-Authorize.md) | Tenant setting, permissions, workspace, accounts, and roles |
| 4 | [Stage 2: Prepare and Connect Data](04-Stage-2-Prepare-and-Connect-Data.md) | Supported lakehouse and ArcGIS source paths |
| 5 | [Stage 3: Build and Style the Map](05-Stage-3-Build-and-Style-the-Map.md) | Item creation, sign-in, layers, and map configuration |
| 6 | [Stage 4: Validate and Operationalize](06-Stage-4-Validate-and-Operationalize.md) | Save/open validation, role testing, gaps, and POC exit criteria |

## Architecture

The documented product behavior establishes a logical architecture with:

- A Fabric tenant setting and workspace
- An ArcGIS Maps for Fabric item
- Microsoft Fabric and ArcGIS Online identities
- Lakehouse, ArcGIS Online, and Living Atlas data-source categories
- Dual authorization requirements for viewing and saving

See [Architecture](Architecture.md) for the evidence-backed logical view and unresolved deployment questions.

## Foundational Requirements

| Requirement | Minimum documented condition |
|---|---|
| Fabric tenant | Tenant administrator enables ArcGIS Maps for Microsoft Fabric |
| Capacity | Workspace capacity sufficient to save workload items; minimum SKU is not published |
| Workspace | Map item is created in a Fabric workspace and location |
| ArcGIS account | ArcGIS Online organizational account; Public accounts are unsupported |
| Author roles | ArcGIS Creator or higher and Fabric Contributor or higher |
| Viewer roles | ArcGIS Viewer or higher and Fabric Viewer or higher |
| API permissions | Azure Storage, Microsoft Graph, and Power BI Service permissions listed in Stage 1 |

## Scope and Boundaries

This area covers current, documented ArcGIS Maps for Microsoft Fabric behavior. It does not claim that:

- Every Fabric data item can be mapped.
- Every ArcGIS layer or service type is supported.
- GeoAnalytics is required to use Maps for Fabric.
- Data moves between Fabric and ArcGIS without an explicit documented path.
- ArcGIS for Power BI and ArcGIS Maps for Microsoft Fabric are interchangeable.
- Identity, networking, or governance behavior matches another ArcGIS integration.
- Maps for Fabric provides GeoAnalytics processing functions.
- A vendor-published deployment or network architecture exists for this workload.

## Supporting Technical Records

| Document | Purpose |
|---|---|
| [Customer Guidance](01-Customer-Guidance.md) | Discovery questions, proof-of-concept framing, and validation boundaries |
| [Architecture](Architecture.md) | Logical product architecture, dependencies, and open deployment questions |
| [Architecture Mapping](Architecture-Mapping.md) | Architecture views and evidence status |
| [Evidence register](records/Evidence.md) | Supported claims and open evidence gaps |
| [Source register](records/Source-Register.md) | Authoritative sources reviewed for this component |
| [Collection checklist](records/Collection-Checklist.md) | Collected artifacts and evidence still required |
| [Public research](records/Public-Research.md) | Authority tiers, naming, findings, and documentation gaps |

## Architecture Status

Published Product Guidance with Open Production Gaps
