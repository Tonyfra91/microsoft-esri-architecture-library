# ArcGIS Maps for Microsoft Fabric Evidence Register

## Purpose

This register maps product and implementation claims to authoritative Microsoft and Esri sources.

## Evidence Inventory

| ID | Architecture claim | Source ID | Source | Status |
|---|---|---|---|---|
| MAP-001 | ArcGIS Maps for Microsoft Fabric is a Fabric workload for creating interactive, multiscale maps within Microsoft Fabric. | SRC-MAP-ESRI-001; SRC-MAP-ESRI-002 | ArcGIS for Microsoft Fabric; Quick Start Guide pp. 3–4 | Supported |
| MAP-002 | A tenant administrator enables the workload; the workspace capacity must be sufficient to save workload items; the product lists required Azure Storage, Microsoft Graph, and Power BI Service permissions. | SRC-MAP-ESRI-002 | Quick Start Guide p. 6 | Supported; no minimum capacity SKU stated |
| MAP-003 | ArcGIS Online organizational accounts are required; Public accounts are unsupported; viewing requires Viewer or higher in ArcGIS and Fabric, while creating or saving requires Creator or higher in ArcGIS and Contributor or higher in Fabric. | SRC-MAP-ESRI-002 | Quick Start Guide pp. 7–9 | Supported |
| MAP-004 | A user creates the item from a Fabric workspace through **+ New item**, chooses a name and location, and signs in to ArcGIS from the new item. | SRC-MAP-ESRI-002 | Quick Start Guide pp. 10–11 | Supported |
| MAP-005 | Documented source categories are Fabric lakehouse, ArcGIS Online, and ArcGIS Living Atlas; supported lakehouse formats include GeoJSON, Parquet or GeoParquet, and CSV with latitude and longitude mapping. | SRC-MAP-ESRI-002 | Quick Start Guide pp. 12–17 | Supported |
| MAP-006 | Documented map configuration includes properties, styles, filters, effects, aggregation, pop-ups, fields, and labels; styles include heat map, counts and amounts, unique symbols, Compare A to B, and dot density. | SRC-MAP-ESRI-002 | Quick Start Guide pp. 19–24 | Supported |
| MAP-007 | The product documents Save, Save as, and open-map workflows; saving requires ArcGIS Creator or higher and Fabric Contributor or higher. | SRC-MAP-ESRI-002 | Quick Start Guide pp. 9, 12, 18–19 | Supported |
| MAP-008 | Esri recommends limiting maps to three or fewer layers for interpretability. | SRC-MAP-ESRI-002 | Quick Start Guide p. 20 | Supported as design guidance |
| MAP-009 | ArcGIS Maps for Microsoft Fabric is listed as generally available in September 2026. | SRC-MAP-MSFT-001; SRC-MAP-MSFT-002 | Microsoft Fabric release notes; GA announcement | Supported for product status; blog content is secondary |

## Open Evidence Gaps

| ID | Gap | Status | Validation need |
|---|---|---|---|
| GAP-001 | Minimum Fabric capacity SKU | Open | Confirm through current product documentation or support |
| GAP-002 | Workload hosting, network endpoints, firewall requirements, and trust boundaries | Open | Obtain Microsoft or Esri security and network documentation |
| GAP-003 | Data movement, caching, refresh, and source-update behavior | Open | Obtain technical documentation and validate in a POC |
| GAP-004 | Data residency, regional processing, and telemetry | Open | Obtain privacy, compliance, and telemetry documentation |
| GAP-005 | Sharing, publishing, and governance beyond Save and Open | Open | Confirm supported product workflow |
| GAP-006 | Dedicated known issues and limitations | Open | Obtain current support or release documentation |
| GAP-007 | Product-specific deployment architecture diagram | Open | No vendor-published diagram found in reviewed sources |

## Last Review Date

2026-10-10

## Owner

Architecture team
