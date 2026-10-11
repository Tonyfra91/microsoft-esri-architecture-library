# ArcGIS Maps for Microsoft Fabric Architecture Mapping

## Purpose

This map connects each architecture view to its current evidence status.

## Architecture Work Products

| Work product | Customer question | Required evidence | Status |
|---|---|---|---|
| Product context | Where does Maps for Fabric fit? | Esri product page and Quick Start Guide | Supported |
| Logical component view | Which documented systems and items participate? | Quick Start requirements and workflows | Supported as a scenario view |
| Source-selection view | How does the user add documented data? | Lakehouse, ArcGIS Online, and Living Atlas workflows | Supported |
| Identity architecture | Which user roles are required? | Fabric and ArcGIS role matrix | Supported |
| Trust-boundary view | What crosses Microsoft, customer, and Esri boundaries? | Endpoint, protocol, telemetry, and data-handling documentation | VALIDATION REQUIRED |
| Minimum POC | What is the smallest supported customer pattern? | Requirements, authoring workflow, and exit criteria | Supported with open production gaps |
| Production operations | How do refresh, sharing, audit, and residency work? | Product administration and security documentation | VALIDATION REQUIRED |

## Relationship to the Library

| From | To | Relationship |
|---|---|---|
| [02 · GeoAnalytics for Fabric](../02-GeoAnalytics-for-Fabric/) | 03 · ArcGIS Maps for Fabric | Spatially prepared data may become an input when the path is supported and validated |
| 03 · ArcGIS Maps for Fabric | [04 · Fabric IQ + Spatial Intelligence](../04-Fabric-IQ-Spatial-Intelligence/) | Map experiences may inform spatial-context exploration; no technical integration is asserted |

## Evidence Rule

Only claims recorded as supported in the [Evidence register](records/Evidence.md) may appear as definitive architecture statements. Scenario views must state what they do not represent. Collection checklist items are not evidence claims.
