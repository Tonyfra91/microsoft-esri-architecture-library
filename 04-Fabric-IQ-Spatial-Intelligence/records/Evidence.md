# Fabric IQ + Spatial Intelligence Evidence Register

## Purpose

This register maps implementation claims to authoritative sources and separates supported Fabric IQ behavior from repository scenario guidance and unresolved Esri integration questions.

## Evidence Inventory

| ID | Architecture claim | Source ID | Source | Status |
|---|---|---|---|---|
| <a id="iq-001"></a>IQ-001 | Fabric IQ is part of Microsoft IQ and provides business context over organizational entities and data. | [SRC-IQ-MSFT-001](Source-Register.md#src-iq-msft-001); [SRC-IQ-MSFT-002](Source-Register.md#src-iq-msft-002) | Microsoft IQ; Fabric IQ overview | Supported |
| <a id="iq-002"></a>IQ-002 | Fabric IQ combines unified data in OneLake, business intelligence through semantic models, and operational intelligence through ontology capabilities. | [SRC-IQ-MSFT-002](Source-Register.md#src-iq-msft-002); [SRC-IQ-MSFT-003](Source-Register.md#src-iq-msft-003) | Fabric IQ overview and getting-started guidance | Supported |
| <a id="iq-003"></a>IQ-003 | Ontology is a preview Fabric item that defines business entities, properties, relationships, rules, and metrics and binds them to enterprise data. | [SRC-IQ-MSFT-004](Source-Register.md#src-iq-msft-004) | Ontology overview | Supported; preview |
| <a id="iq-004"></a>IQ-004 | An ontology can be created from scratch, generated or aligned from a semantic model, and imported from supported open standards such as RDF or OWL. | [SRC-IQ-MSFT-002](Source-Register.md#src-iq-msft-002); [SRC-IQ-MSFT-004](Source-Register.md#src-iq-msft-004) | Fabric IQ and ontology overviews | Supported; preview |
| <a id="iq-005"></a>IQ-005 | Creating ontology items requires the tenant settings **Users can create Fabric items** and **Users can create ontology (preview) items**. | [SRC-IQ-MSFT-005](Source-Register.md#src-iq-msft-005) | Ontology tenant settings | Supported; preview |
| <a id="iq-006"></a>IQ-006 | The Microsoft ontology tutorial creates entities and relationships, binds static and streaming data, and explores the result with built-in graph and ontology-agent experiences. | [SRC-IQ-MSFT-006](Source-Register.md#src-iq-msft-006) | Ontology tutorial | Supported as Microsoft tutorial behavior |
| <a id="iq-007"></a>IQ-007 | An ontology can optionally generate a graph model for relationship-centric exploration and queries. | [SRC-IQ-MSFT-008](Source-Register.md#src-iq-msft-008); [SRC-IQ-MSFT-009](Source-Register.md#src-iq-msft-009) | Ontology graph and Fabric Graph documentation | Supported; ontology integration is preview |
| <a id="iq-008"></a>IQ-008 | The ontology agent supports natural-language assistance for ontology creation, binding, questions, and proposal-first changes. | [SRC-IQ-MSFT-007](Source-Register.md#src-iq-msft-007) | Ontology agent documentation | Supported; preview |
| <a id="iq-009"></a>IQ-009 | Fabric Data Agents provide natural-language access to supported Fabric data sources and can be consumed by other supported experiences. | [SRC-IQ-MSFT-011](Source-Register.md#src-iq-msft-011); [SRC-IQ-MSFT-012](Source-Register.md#src-iq-msft-012) | Fabric Data Agent and Foundry integration documentation | Supported; integration is preview where documented |
| <a id="iq-010"></a>IQ-010 | This library's minimum spatial-intelligence scenario persists spatially derived relationships in OneLake before binding them into an ontology. | [02 · GeoAnalytics for Fabric](../../02-GeoAnalytics-for-Fabric/); [SRC-IQ-MSFT-004](Source-Register.md#src-iq-msft-004) | Repository synthesis using supported GeoAnalytics outputs and ontology bindings | Supported as conservative scenario guidance |
| <a id="iq-011"></a>IQ-011 | ArcGIS Maps for Fabric may visualize the same governed Lakehouse data used by the ontology, but no direct ArcGIS Maps-to-Fabric-IQ integration is asserted. | [03 · ArcGIS Maps for Fabric](../../03-ArcGIS-Maps-for-Fabric/); [SRC-IQ-MSFT-004](Source-Register.md#src-iq-msft-004) | Repository synthesis of separate supported product paths | Supported as architecture boundary |

## Open Evidence Gaps

| ID | Gap | Status | Validation need |
|---|---|---|---|
| <a id="gap-iq-001"></a>GAP-IQ-001 | Direct Esri product integration with Fabric IQ ontology | Open | Obtain Microsoft and Esri product documentation or engineering confirmation |
| <a id="gap-iq-002"></a>GAP-IQ-002 | Native geometry types, spatial predicates, and dynamic spatial relationships in ontology | Open | Confirm current ontology spatial capabilities |
| <a id="gap-iq-003"></a>GAP-IQ-003 | Production refresh, schema evolution, rebinding, and lifecycle behavior | Open | Validate current preview behavior and roadmap |
| <a id="gap-iq-004"></a>GAP-IQ-004 | Production licensing, support, regional availability, and service limits | Open | Confirm current preview and commercial terms |
| <a id="gap-iq-005"></a>GAP-IQ-005 | Semantic mapping of Utility Network or other Esri domain models | Open | Complete authoritative Esri artifact discovery and semantic-equivalence review |

## Last Review Date

2026-10-11

## Owner

Architecture team
