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

### Tier 2: Vendor blogs and community resources

- Microsoft Fabric Community general-availability announcement
- Microsoft Fabric Updates blog
- Esri ArcGIS Blog posts
- Esri Community announcements and category hub

Tier 2 sources can establish chronology, product messaging, and implementation observations. Technical architecture claims require Tier 1 support or explicit engineering confirmation.

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

2026-10-10
