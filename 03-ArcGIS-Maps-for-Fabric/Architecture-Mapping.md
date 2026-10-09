# ArcGIS Maps for Microsoft Fabric Architecture Mapping

## Purpose

This map connects each planned architecture section to the evidence needed to publish it.

## Architecture Work Products

| Work product | Customer question | Required evidence | Status |
|---|---|---|---|
| Product context | Where does Maps for Fabric fit? | Microsoft and Esri product documentation | SOURCE REQUIRED |
| Component architecture | What runs where? | Product boundary and platform dependencies | VALIDATION REQUIRED |
| Data-flow architecture | How does supported data reach the map? | Supported sources, access mode, refresh, and output behavior | VALIDATION REQUIRED |
| Identity architecture | How do users and services authenticate and authorize? | Fabric and ArcGIS identity documentation | VALIDATION REQUIRED |
| Trust-boundary view | What crosses Microsoft, customer, and Esri boundaries? | Endpoint, protocol, telemetry, and data-handling documentation | VALIDATION REQUIRED |
| Minimum POC | What is the smallest supported customer pattern? | Prerequisites, setup guidance, and a validated scenario | VALIDATION REQUIRED |

## Relationship to the Library

| From | To | Relationship |
|---|---|---|
| [02 · GeoAnalytics for Fabric](../02-GeoAnalytics-for-Fabric/) | 03 · ArcGIS Maps for Fabric | Spatially prepared data may become an input when the path is supported and validated |
| 03 · ArcGIS Maps for Fabric | [04 · Fabric IQ + Spatial Intelligence](../04-Fabric-IQ-Spatial-Intelligence/) | Map experiences may inform spatial-context exploration; no technical integration is asserted |

## Evidence Rule

Only claims recorded as supported in the [Evidence register](records/Evidence.md) may appear as definitive architecture statements. Collection checklist items are not evidence claims.
