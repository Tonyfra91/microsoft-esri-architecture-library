# Fabric IQ + Spatial Intelligence Architecture Mapping

## Purpose

This map connects each architecture view to its evidence status and implementation page.

## Architecture Work Products

| Work product | Customer question | Evidence | Status |
|---|---|---|---|
| Product context | Where does Fabric IQ fit after spatial processing and visualization? | [IQ-001](records/Evidence.md#iq-001); [IQ-002](records/Evidence.md#iq-002) | Supported |
| Foundational requirements | Which tenant, workspace, source, and preview settings are required? | [IQ-005](records/Evidence.md#iq-005); [GAP-IQ-004](records/Evidence.md#gap-iq-004) | Supported with preview validation |
| Entity and relationship model | Which bounded business concepts answer the POC question? | [IQ-003](records/Evidence.md#iq-003); [IQ-010](records/Evidence.md#iq-010) | Supported as scenario guidance |
| Ontology binding | How are business definitions connected to governed data? | [IQ-003](records/Evidence.md#iq-003); [IQ-004](records/Evidence.md#iq-004) | Supported; preview |
| Graph exploration | When should relationships be materialized as a graph? | [IQ-007](records/Evidence.md#iq-007) | Optional; preview |
| Ontology agent | How can users ask questions and review proposed changes? | [IQ-008](records/Evidence.md#iq-008) | Supported; preview |
| ArcGIS Maps relationship | How does the map experience relate to ontology data? | [IQ-011](records/Evidence.md#iq-011) | Shared governed data; no direct integration asserted |
| Esri domain mapping | Can Utility Network or another Esri model map to ontology? | [GAP-IQ-005](records/Evidence.md#gap-iq-005) | Advanced research track |
| Production operations | How do refresh, scale, lineage, support, and lifecycle work? | [GAP-IQ-003](records/Evidence.md#gap-iq-003); [GAP-IQ-004](records/Evidence.md#gap-iq-004) | VALIDATION REQUIRED |

## Relationship to the Library

| From | To | Relationship |
|---|---|---|
| [02 · GeoAnalytics for Fabric](../02-GeoAnalytics-for-Fabric/) | 04 · Fabric IQ + Spatial Intelligence | GeoAnalytics may persist required spatial relationships in governed OneLake tables |
| [03 · ArcGIS Maps for Fabric](../03-ArcGIS-Maps-for-Fabric/) | 04 · Fabric IQ + Spatial Intelligence | ArcGIS Maps may visualize the same governed data through a separate supported path |
| 04 · Fabric IQ + Spatial Intelligence | [05 · Microsoft + Esri Agentic Reference Pattern](../05-Microsoft-Esri-Agentic-Reference-Pattern/) | Validated entities, relationships, authority, and lineage can ground a later agentic pattern |

## Evidence Rule

Only supported Microsoft product behavior is stated as definitive. Spatial relationship preparation is repository scenario guidance based on GeoAnalytics outputs. No direct Esri-to-Fabric-IQ connection may be drawn as supported until authoritative evidence exists.
