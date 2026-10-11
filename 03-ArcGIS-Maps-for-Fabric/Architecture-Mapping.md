# ArcGIS Maps for Microsoft Fabric Architecture Mapping

## Purpose

This map connects each architecture view to its current evidence status.

## Architecture Work Products

| Work product | Customer question | Required evidence | Status |
|---|---|---|---|
| Product context | Where does Maps for Fabric fit? | Esri product page and Quick Start Guide | Supported |
| Logical reference architecture | Which documented systems, identities, sources, and artifacts participate? | Quick Start requirements and workflows | Supported as a logical scenario view; not a deployment or network architecture |
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

## Visual Work Products

| Visual | Location | Classification |
|---|---|---|
| Three-product selection | [Customer Guidance](01-Customer-Guidance.md#choose-the-right-spatial-experience) | Customer decision aid |
| Map-authoring scenario flow | [End-to-End Scenario](02-End-to-End-Scenario.md#where-arcgis-maps-appears-in-fabric) | Scenario flow, not reference architecture |
| Four-stage POC lifecycle | [End-to-End Scenario](02-End-to-End-Scenario.md#the-scenario-at-a-glance) | Implementation lifecycle |
| Logical reference architecture | [Architecture](Architecture.md#evidence-backed-logical-reference-architecture) | Evidence-backed logical scenario view |
| Dual identity and authorization | [Stage 1](03-Stage-1-Enable-and-Authorize.md#role-matrix) | Access-requirement view |
| Source selection | [Stage 2](04-Stage-2-Prepare-and-Connect-Data.md#supported-source-categories) | Documented source-path view |
| Representative outcome map | [Stage 3](05-Stage-3-Build-and-Style-the-Map.md#representative-outcome-map) | Planned illustrative outcome |
| Production validation gates | [Stage 4](06-Stage-4-Validate-and-Operationalize.md#production-validation) | Governance and readiness view |
