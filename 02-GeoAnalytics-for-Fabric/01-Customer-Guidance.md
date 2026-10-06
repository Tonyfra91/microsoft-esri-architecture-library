# ArcGIS GeoAnalytics for Microsoft Fabric: Customer Guidance

## Executive Summary

ArcGIS GeoAnalytics for Microsoft Fabric runs distributed spatial analysis inside Microsoft Fabric Spark, so Esri and business data can be enriched where it already lives. This page gives the reference pattern, what a customer needs in place to run it, the three stages of the scenario, and how to scope a proof of concept. For the full landscape, see [01 · Microsoft + Esri Foundation](../01-Microsoft-Esri-Foundation/).

---

## Where GeoAnalytics Sits in the Microsoft + Esri Landscape

The Microsoft + Esri landscape is anchored by five integrations. Three run in Microsoft Fabric and Power BI: **ArcGIS GeoAnalytics for Microsoft Fabric**, **ArcGIS Maps for Microsoft Fabric**, and **ArcGIS for Power BI**. Two extend the story: **ArcGIS for Microsoft 365** and **ArcGIS on Microsoft Azure**. The full landscape is described in [01 · Microsoft + Esri Foundation](../01-Microsoft-Esri-Foundation/README.md#microsoft--esri-fabric-integration-landscape).

Within that landscape, GeoAnalytics provides the **spatial processing** step:

| Capability | Role in the landscape | Covered in |
|---|---|---|
| **ArcGIS GeoAnalytics for Microsoft Fabric** | Distributed spatial analysis and enrichment in Fabric Spark | This guide |
| ArcGIS Maps for Microsoft Fabric | Mapping and spatial visualization within Fabric | Planned component 03 |
| ArcGIS for Power BI | Location-aware reporting for business users | Planned component 04 |

These capabilities are related but not interchangeable. GeoAnalytics typically produces the spatially enriched data that the mapping and reporting experiences consume.

---

## Reference Pattern

![Microsoft Esri Simplified Solution Pattern](images/microsoft-esri-simplified-solution-pattern.png)

In this pattern:

- Microsoft Fabric and OneLake provide the shared data and analytics foundation.
- Fabric Spark notebooks and Spark job definitions provide the processing environment. This is where ArcGIS GeoAnalytics runs and adds spatial processing and enrichment.
- ArcGIS Maps for Microsoft Fabric and ArcGIS for Power BI serve the results as distinct consumption experiences.
- Spatially enriched data products can support downstream analytics and separately validated AI scenarios.

> **Diagram note:** The Esri components (ArcGIS data sources, GeoAnalytics in the Spark notebooks, ArcGIS Maps for Fabric and ArcGIS for Power BI in Serve, and the Esri licensing service outside Fabric) are being added to this diagram.

This pattern supports architecture discovery and proof-of-concept planning. It is not a prescriptive deployment design. Customer-specific decisions on data sources, identity, networking, security, workspace topology, capacity, operations, and consumption experiences require separate validation.

**Architecture type:** Simplified solution pattern  
**Contributor:** Nick Snapp  
**Usage:** Customer architecture discussions and initial proof-of-concept framing

---

## What You Need to Run GeoAnalytics

GeoAnalytics is not a standalone service. It runs only inside Microsoft Fabric, so a Fabric foundation is the first requirement. The minimum, as published by Microsoft and Esri:

| # | Requirement | What it means | Source |
|---|---|---|---|
| 1 | **Microsoft Fabric capacity and workspace** | A Fabric workspace on a capacity where Spark can run. Published documentation does not state a minimum capacity size; confirm during discovery. | [Microsoft Learn](https://learn.microsoft.com/en-us/fabric/data-engineering/spark-arcgis-geoanalytics) |
| 2 | **Tenant setting enabled** | A Fabric tenant administrator enables *ArcGIS GeoAnalytics for Fabric Runtime* in the Admin Portal. Capacity administrators can override it per capacity. When disabled, the library is unavailable. | [Microsoft Learn](https://learn.microsoft.com/en-us/fabric/data-engineering/spark-arcgis-geoanalytics); [Evidence SEC-001](records/Evidence.md) |
| 3 | **Fabric Runtime 1.3** | GeoAnalytics is enabled only in the Fabric 1.3 runtime. The library is preinstalled and preconfigured; no separate installation. | [Esri FAQ](https://developers.arcgis.com/geoanalytics-fabric/faq/); [Microsoft Learn](https://learn.microsoft.com/en-us/fabric/data-engineering/spark-arcgis-geoanalytics) |
| 4 | **OneLake data** | A Lakehouse or other supported Fabric data source to read input from and write enriched results back to. | [Microsoft Learn](https://learn.microsoft.com/en-us/fabric/data-engineering/spark-arcgis-geoanalytics) |
| 5 | **Spark notebook or Spark job definition** | Where GeoAnalytics code runs (`import geoanalytics_fabric`). | [Esri FAQ](https://developers.arcgis.com/geoanalytics-fabric/faq/) |
| 6 | **GeoAnalytics license** | Bring your own license: an active GeoAnalytics for Microsoft Fabric subscription, authorized with a username and password or an Esri-provided API key. Usage is metered in compute unit-hours (core-hours). | [Microsoft Learn](https://learn.microsoft.com/en-us/fabric/data-engineering/spark-arcgis-geoanalytics); [Esri authorization](https://developers.arcgis.com/geoanalytics-fabric/authorization/) |
| 7 | **Outbound HTTPS to Esri** | Outbound HTTPS on port 443 to arcgis.com for authorization and usage reporting. Not supported when Outbound Access Protection is enabled. | [Evidence SEC-004, SEC-007](records/Evidence.md) |

The [Stage 2 minimum deployable POC diagram](04-Stage-2-Spatial-Processing.md#architecture) shows these requirements in one view, with the calls that cross the Fabric boundary.

**Platform references:**

- **Fabric platform architecture:** [Analytics end-to-end with Microsoft Fabric](https://learn.microsoft.com/en-us/azure/architecture/example-scenario/dataplate2e/data-platform-end-to-end) (Microsoft Learn) shows how Fabric ingests, governs, stores, processes, and serves data.
- **GeoAnalytics component architecture:** [Architecture.md](Architecture.md) shows how GeoAnalytics sits within Fabric (Fabric, Fabric Runtime, Apache Spark, GeoAnalytics) and its dependencies.

---

## The Three Stages

The scenario moves through three stages. Each stage has its own page with discovery questions, flow, architecture, guidance, and handoff. The [End-to-End Scenario](02-End-to-End-Scenario.md) walks through them in order.

```text
Stage 1 · Bring data into Fabric
  Customer data sources → Fabric ingestion or supported connection → OneLake and Fabric data items

Stage 2 · Spatial processing
  Fabric Spark notebook or Spark job definition → ArcGIS GeoAnalytics → Spatially enriched Spark DataFrame

Stage 3 · Use the results
  Customer-approved Fabric or ArcGIS output → Power BI, ArcGIS Maps for Fabric, or ArcGIS apps
```

| Stage | Outcome | Page |
|---|---|---|
| 1 · Bring data into Fabric | Business and spatial data available in OneLake, copied in or read in place from ArcGIS | [Stage 1](03-Stage-1-Bring-Data-into-Fabric.md) |
| 2 · Spatial processing | GeoAnalytics enriches the data in Fabric Spark | [Stage 2](04-Stage-2-Spatial-Processing.md) |
| 3 · Use the results | Enriched output reviewed in the selected consumption experience | [Stage 3](05-Stage-3-Use-the-Results.md) |

---

## Proof-of-Concept Framework

A proof of concept should begin with a clearly defined business decision or analytical question that requires location context. The architecture should then be reduced to the minimum components required to test that question.

A bounded GeoAnalytics proof of concept should identify:

1. **Business question**  
   The operational, analytical, or planning decision that requires location intelligence.

2. **Authoritative business data**  
   The customer dataset representing the relevant asset, event, customer, transaction, or operational condition.

3. **Authoritative geospatial data**  
   The layers, features, boundaries, files, services, or other spatial sources required to provide location context.

4. **Fabric landing or access point**  
   The approved Fabric location or supported connection through which the required data will be accessed.

5. **Spatial operation**  
   The documented GeoAnalytics function or analysis tool required to answer the business question.

6. **Validated output**  
   The spatially enriched dataset, analytical result, or measurable finding the proof of concept is expected to produce.

7. **Consumption experience**  
   The validated experience through which the output will be reviewed, such as Power BI, an ArcGIS application, ArcGIS Maps for Microsoft Fabric, or an approved Fabric data product.

8. **Success criteria**  
   The measurable result that would demonstrate business value, architectural fit, and technical feasibility.

### Network Readiness Discovery

Confirm the customer's network posture early. GeoAnalytics calls Esri services outside Fabric for authentication and usage tracking, and is currently not supported when Outbound Access Protection is enabled ([Evidence SEC-004](records/Evidence.md)). Esri confirms these calls use HTTPS on port 443 to the arcgis.com domain, and that notebook plotting with a basemap also retrieves tiles from Esri ([Evidence SEC-007 to SEC-009](records/Evidence.md)). Behavior with managed virtual networks or Private Link is not yet documented ([Evidence GAP-003](records/Evidence.md#open-evidence-gaps)).

- [ ] Is Outbound Access Protection enabled, or planned, for the target Fabric workspace?
- [ ] Is outbound internet access from Fabric Spark restricted by customer firewall or proxy policy?
- [ ] Does the customer require endpoint or hostname allow-listing for outbound connections? If so, allow outbound HTTPS on port 443 to arcgis.com. *(SEC-007)*
- [ ] Does the target workspace use managed virtual networks or Private Link? *(Open: GeoAnalytics behavior not yet documented, GAP-003)*
- [ ] Has the customer's network or security team been engaged to review these requirements before the proof of concept?

If any answer indicates restricted outbound access, raise it as a proof-of-concept risk and escalate to Esri and Microsoft for confirmation before committing to a design.

The objective is not to demonstrate every Microsoft and Esri integration in a single exercise. The objective is to validate a focused and repeatable pattern that can inform a production design.

---

## Scope and Boundaries

This guide describes the documented current-state relationship between Microsoft Fabric and ArcGIS GeoAnalytics for Microsoft Fabric. It does not claim that:

- Every ArcGIS product, service, or data model runs within Microsoft Fabric.
- ArcGIS GeoAnalytics replaces ArcGIS applications or operational GIS systems.
- ArcGIS Online or ArcGIS Enterprise data automatically synchronizes with OneLake.
- ArcGIS Maps for Microsoft Fabric and ArcGIS for Power BI are interchangeable.
- A spatially enriched Fabric dataset is automatically available to copilots or agents.
- GeoIQ, ArcGIS MCP, Microsoft Foundry, or agentic integrations are included in the current GeoAnalytics product architecture.

Agentic, GeoIQ, and MCP integration concepts should be documented separately as reference patterns until their product behavior, identity model, security boundaries, and supported integration paths are validated.

---

## Supporting Technical Records

- [End-to-end scenario walkthrough](02-End-to-End-Scenario.md)
- [Component architecture](Architecture.md)
- [Evidence register](records/Evidence.md)
- [Source register](records/Source-Register.md)
