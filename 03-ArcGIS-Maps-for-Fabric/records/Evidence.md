# ArcGIS Maps for Microsoft Fabric Evidence Register

## Purpose

This register maps product and implementation claims to authoritative Microsoft and Esri sources.

## Evidence Inventory

| ID | Architecture claim | Source ID | Source | Status |
|---|---|---|---|---|
| <a id="map-001"></a>MAP-001 | ArcGIS Maps for Microsoft Fabric is a Fabric workload for creating interactive, multiscale maps within Microsoft Fabric. | SRC-MAP-ESRI-001; SRC-MAP-ESRI-002 | ArcGIS for Microsoft Fabric; Quick Start Guide pp. 3–4 | Supported |
| <a id="map-002"></a>MAP-002 | A tenant administrator enables the workload; the workspace capacity must be sufficient to save workload items; the product lists required Azure Storage, Microsoft Graph, and Power BI Service permissions. | SRC-MAP-ESRI-002 | Quick Start Guide p. 6 | Supported; no minimum capacity SKU stated |
| <a id="map-003"></a>MAP-003 | ArcGIS Online organizational accounts are required; Public accounts are unsupported; viewing requires Viewer or higher in ArcGIS and Fabric, while creating or saving requires Creator or higher in ArcGIS and Contributor or higher in Fabric. | SRC-MAP-ESRI-002 | Quick Start Guide pp. 7–9 | Supported |
| <a id="map-004"></a>MAP-004 | A user creates the item from a Fabric workspace through **+ New item**, chooses a name and location, and signs in to ArcGIS from the new item. | SRC-MAP-ESRI-002 | Quick Start Guide pp. 10–11 | Supported |
| <a id="map-005"></a>MAP-005 | Documented source categories are Fabric lakehouse, ArcGIS Online, and ArcGIS Living Atlas; supported lakehouse formats include GeoJSON, Parquet or GeoParquet, and CSV with latitude and longitude mapping. | SRC-MAP-ESRI-002 | Quick Start Guide pp. 12–17 | Supported |
| <a id="map-006"></a>MAP-006 | Documented map configuration includes properties, styles, filters, effects, aggregation, pop-ups, fields, and labels; styles include heat map, counts and amounts, unique symbols, Compare A to B, and dot density. | SRC-MAP-ESRI-002 | Quick Start Guide pp. 19–24 | Supported |
| <a id="map-007"></a>MAP-007 | The product documents Save, Save as, and open-map workflows; saving requires ArcGIS Creator or higher and Fabric Contributor or higher. | SRC-MAP-ESRI-002 | Quick Start Guide pp. 9, 12, 18–19 | Supported |
| <a id="map-008"></a>MAP-008 | Esri recommends limiting maps to three or fewer layers for interpretability. | SRC-MAP-ESRI-002 | Quick Start Guide p. 20 | Supported as design guidance |
| <a id="map-009"></a>MAP-009 | ArcGIS Maps for Microsoft Fabric is listed as generally available in September 2026. | SRC-MAP-MSFT-001; SRC-MAP-MSFT-002 | Microsoft Fabric release notes; GA announcement | Supported for product status; blog content is secondary |
| <a id="map-010"></a>MAP-010 | The GA announcement describes ArcGIS Online Stream Layer support, direct Parquet use from OneLake, and symbol, label, and sketch enhancements. | SRC-MAP-MSFT-002 | Microsoft Fabric Community GA announcement | Secondary product evidence; technical architecture implications require Tier 1 documentation |
| <a id="map-011"></a>MAP-011 | ArcGIS for Power BI is a visualization used on a Power BI report page in Power BI Desktop or the Power BI service; report consumers can interact with the visual through supported Power BI report features. | SRC-MAP-MSFT-004; SRC-MAP-MSFT-005 | Microsoft Learn author and consumer guidance | Supported |
| <a id="map-012"></a>MAP-012 | ArcGIS for Power BI supports limited guest use and organizational ArcGIS sign-in; Public accounts are unsupported; ArcGIS Enterprise 10.8.1 and later is supported in connected environments; secured content and report publishing have additional identity and licensing requirements. | SRC-MAP-ESRI-010; SRC-MAP-ESRI-011; SRC-MAP-MSFT-004 | Esri account and sign-in documentation; Microsoft Learn | Supported; capability depends on privileges and licensing |
| <a id="map-013"></a>MAP-013 | Choose Maps for Fabric for a dedicated Fabric map item and ArcGIS for Power BI for a map embedded in a Power BI report. The products can serve different audiences but their artifacts and sharing models are not assumed to be interchangeable. | SRC-MAP-ESRI-001; SRC-MAP-ESRI-002; SRC-MAP-ESRI-010; SRC-MAP-ESRI-011; SRC-MAP-MSFT-004; SRC-MAP-MSFT-005 | Repository synthesis of documented product boundaries | Supported as selection guidance |
| <a id="map-014"></a>MAP-014 | Microsoft Fabric Maps is a first-class Fabric workspace item for real-time and historical location data. It supports Eventhouse or KQL, lakehouse, external feature services including Esri Feature Service endpoints, and external imagery. | SRC-MAP-MSFT-006; SRC-MAP-MSFT-007 | Microsoft Learn Fabric Maps overview and creation guidance | Supported |
| <a id="map-015"></a>MAP-015 | A user with item-creation permission in a Fabric-enabled workspace creates a native Map through **+ New item**; the saved map participates in Fabric workspace permissions, sharing, governance, and lifecycle management. | SRC-MAP-MSFT-006; SRC-MAP-MSFT-007 | Microsoft Learn Fabric Maps overview and creation guidance | Supported |
| <a id="map-016"></a>MAP-016 | Fabric Maps uses Fabric capacity units without a separate map-specific license or SKU. Azure Maps services or notebooks perform spatial computation, while Fabric Maps presents the resulting insights. | SRC-MAP-MSFT-006 | Microsoft Learn Fabric Maps overview | Supported |
| <a id="map-017"></a>MAP-017 | Choose ArcGIS Maps for Fabric for a dedicated ArcGIS map and cartographic workflow, Microsoft Fabric Maps for Eventhouse-centered operational monitoring, and ArcGIS for Power BI for a map embedded in a report. The products may coexist, but their artifacts, identities, refresh models, and sharing behavior are not interchangeable. | SRC-MAP-ESRI-001; SRC-MAP-ESRI-002; SRC-MAP-MSFT-004; SRC-MAP-MSFT-005; SRC-MAP-MSFT-006; SRC-MAP-MSFT-007 | Repository synthesis of documented product boundaries | Supported as selection guidance |

## Open Evidence Gaps

| ID | Gap | Status | Validation need |
|---|---|---|---|
| <a id="gap-001"></a>GAP-001 | Minimum Fabric capacity SKU | Open | Confirm through current product documentation or support |
| <a id="gap-002"></a>GAP-002 | Workload hosting, network endpoints, firewall requirements, and trust boundaries | Open | Obtain Microsoft or Esri security and network documentation |
| <a id="gap-003"></a>GAP-003 | Data movement, caching, refresh, and source-update behavior | Open | Obtain technical documentation and validate in a POC |
| <a id="gap-004"></a>GAP-004 | Data residency, regional processing, and telemetry | Open | Obtain privacy, compliance, and telemetry documentation |
| <a id="gap-005"></a>GAP-005 | Sharing, publishing, and governance beyond Save and Open | Open | Confirm supported product workflow |
| <a id="gap-006"></a>GAP-006 | Dedicated known issues and limitations | Open | Obtain current support or release documentation |
| <a id="gap-007"></a>GAP-007 | Product-specific deployment architecture diagram | Open | No vendor-published diagram found in reviewed sources |

## Last Review Date

2026-10-11

## Owner

Architecture team
