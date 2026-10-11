# ArcGIS Maps for Microsoft Fabric Public Research

## Purpose

This record consolidates the public-source research used to shape the implementation walkthrough. It distinguishes authoritative product documentation from announcements, blogs, related products, and unresolved gaps.

## Product Naming

Public resources use similar names for distinct capabilities:

| Name | Scope |
|---|---|
| ArcGIS Maps for Microsoft Fabric or ArcGIS Maps for Fabric | Esri mapping workload and saved item experience in Fabric; the subject of this component |
| ArcGIS GeoAnalytics for Microsoft Fabric | Spark library for spatial processing in Fabric notebooks and Spark job definitions |
| Fabric Maps or Map item | Microsoft Real-Time Intelligence map experience based on Azure Maps; not the Esri workload |
| ArcGIS for Power BI | Power BI visual; not the Fabric workload |
| ArcGIS for Microsoft Fabric | Esri umbrella offering that includes Maps for Fabric, GeoAnalytics for Fabric, and ArcGIS for Power BI |

Claims from one product must not be transferred to another without product-specific evidence.

## Authority Tiers

### Tier 1: Authoritative product and architecture sources

- Esri's *ArcGIS Maps for Microsoft Fabric Quick Start Guide*
- Esri's *ArcGIS for Microsoft Fabric* product page
- Esri's *ArcGIS for Microsoft* overview
- Esri Architecture Center's *Microsoft and ArcGIS integrations*
- Microsoft Learn release notes for Microsoft Fabric
- Microsoft Learn overview and creation guidance for Microsoft Fabric Maps
- Microsoft Learn author and consumer guidance for ArcGIS for Power BI
- Esri account and sign-in documentation for ArcGIS for Power BI

### Tier 2: Vendor blogs and community resources

- Microsoft Fabric Community general-availability announcement
- Microsoft Fabric Updates blog
- Esri ArcGIS Blog posts
- Esri Community announcements and category hub

Tier 2 sources can establish chronology, product messaging, and implementation observations. Technical architecture claims require Tier 1 support or explicit engineering confirmation.

## Product Selection Findings

ArcGIS Maps for Fabric, Microsoft Fabric Maps, and ArcGIS for Power BI are not
interchangeable authoring surfaces:

- Maps for Fabric produces a dedicated item in a Fabric workspace.
- Microsoft Fabric Maps produces a native Map item in a Fabric workspace.
- ArcGIS for Power BI produces a map visual within a Power BI report.
- Maps for Fabric documents lakehouse selection through the OneLake catalog.
- Microsoft Fabric Maps documents Eventhouse or KQL, lakehouse, Ontology,
  external feature service, and external imagery layers.
- ArcGIS for Power BI uses data fields supplied by the Power BI report.
- Maps for Fabric documents an ArcGIS Online organizational-account
  requirement.
- Microsoft Fabric Maps uses Fabric identity and workspace permissions; an
  ArcGIS identity is not required for native sources.
- ArcGIS for Power BI supports limited guest use and organizational sign-in to
  ArcGIS Online or supported connected ArcGIS Enterprise deployments.
- Maps for Fabric supports ArcGIS Online Stream Layers, but Microsoft Fabric
  Maps provides the native Eventhouse refresh model for operational monitoring.
- Microsoft Fabric Maps can consume Esri Feature Service endpoints, but this
  interoperability does not make it an Esri-authored experience.
- Power BI report distribution and interaction behavior must not be assigned
  to a Maps for Fabric item without product-specific evidence.

The customer should select the intended consumption experience before starting
the Maps for Fabric POC. A solution may use more than one product for different
audiences, but direct artifact portability is not documented.

## General-Availability Announcement Findings

The public Microsoft Fabric Community announcement includes demonstrations of:

- General map authoring in the Fabric workload
- Adding and configuring ArcGIS Online Stream Layers
- Visualizing Parquet data from OneLake
- Symbol animation, label positioning, and sketching enhancements

The article states that Parquet data can be used from OneLake without data
movement or duplication. This is a Tier 2 claim. It does not close the
data-movement, caching, refresh, residency, or network architecture gaps
without corresponding technical documentation.

The repository includes the four public GIF images from the announcement as
interface examples. The public platform delivers each file as a single-frame
GIF. Only assets delivered through the public article are included.

## Authoritative Findings

The September 2026 Quick Start Guide supports:

- Tenant administrator enablement
- Required Azure Storage, Microsoft Graph, and Power BI Service permissions
- Fabric capacity and workspace prerequisites
- ArcGIS Online organizational-account requirements
- Dual ArcGIS and Fabric role requirements
- Item creation and ArcGIS sign-in workflow
- Lakehouse, ArcGIS Online, and Living Atlas source categories
- GeoJSON, Parquet or GeoParquet, and CSV lakehouse formats
- Save, Save as, and open behavior
- Styling, aggregation, effects, labels, fields, pop-ups, and filtering
- A recommendation to use three or fewer layers

## Confirmed Documentation Gaps

No authoritative public source was found for:

- A product-specific deployment or network architecture diagram
- Minimum Fabric capacity SKU
- Complete licensing and pricing interpretation
- Network egress or firewall allow list
- Data residency and regional processing controls
- Telemetry and audit behavior
- Refresh, caching, or source-update semantics
- A complete sharing or publishing workflow
- A dedicated known-issues or limitations page

These gaps justify a POC validation stage. They do not justify inferred architecture claims.

## Recommended Documentation Model

A four-stage walkthrough is appropriate:

1. Enable and authorize.
2. Prepare and connect data.
3. Build and style the map.
4. Validate and operationalize.

This model separates administrative, data, authoring, and production-readiness responsibilities while remaining traceable to the vendor workflow.

## Last Review Date

2026-10-11
