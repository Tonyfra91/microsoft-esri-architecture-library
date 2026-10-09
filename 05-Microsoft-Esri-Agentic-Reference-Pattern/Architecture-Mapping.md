# Microsoft + Esri Agentic Reference Pattern Architecture Mapping

## Purpose

This map ties each conceptual architecture interaction to the evidence needed before it can become a supported reference pattern.

## Interaction Mapping

| Interaction | Evidence needed | Status |
|---|---|---|
| Human to agent | Supported experience, authentication, and session model | SOURCE REQUIRED |
| Agent to Foundry model | Foundry agent and model architecture | SOURCE REQUIRED |
| Agent to Fabric IQ context | Supported Fabric IQ integration and authorization | VALIDATION REQUIRED |
| Agent to Fabric Data Agent | Supported integration contract and identity flow | VALIDATION REQUIRED |
| Agent to semantic model | Supported query path and row-level security behavior | VALIDATION REQUIRED |
| Agent to ArcGIS MCP | MCP documentation, tool schemas, transport, and identity | SOURCE REQUIRED |
| ArcGIS MCP to ArcGIS services | Supported endpoints, permissions, and data handling | VALIDATION REQUIRED |
| Agent to action | Tool contract, side effects, approval, and rollback | VALIDATION REQUIRED |
| Agent to Ground Truth | Source authority, lineage, freshness, and conflict policy | CONCEPTUAL PATTERN |
| System to audit and evaluation | Logging, tracing, evaluation, retention, and governance | SOURCE REQUIRED |

## Evidence Gates

An interaction may be drawn as supported only when:

1. Both endpoints are supported products or validated components.
2. The integration path is documented.
3. Identity and authorization behavior are known.
4. Data and network boundaries are documented.
5. Failure and audit behavior are defined.
6. Security and engineering reviewers approve the interpretation.

## Relationship to the Library

| Input area | Contribution to the pattern |
|---|---|
| [01 · Microsoft + Esri Foundation](../01-Microsoft-Esri-Foundation/) | Platform and portfolio context |
| [02 · GeoAnalytics for Fabric](../02-GeoAnalytics-for-Fabric/) | Evidence-backed spatial processing |
| [03 · ArcGIS Maps for Fabric](../03-ArcGIS-Maps-for-Fabric/) | Spatial experience after validation |
| [04 · Fabric IQ + Spatial Intelligence](../04-Fabric-IQ-Spatial-Intelligence/) | Candidate business and spatial context after validation |
