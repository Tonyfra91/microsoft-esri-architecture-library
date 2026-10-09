# Fabric IQ + Spatial Intelligence Architecture Mapping

## Purpose

This map organizes the research needed before a spatial-intelligence reference architecture can be proposed.

## Exploration Map

| Architecture concern | Microsoft artifact needed | Esri artifact needed | Status |
|---|---|---|---|
| Business entities | Fabric IQ ontology definition | Utility Network entity definitions | SOURCE REQUIRED |
| Properties | Ontology property model | Asset, network, and domain properties | SOURCE REQUIRED |
| Relationships | Fabric IQ relationship and graph model | Connectivity, containment, association, and domain relationships | ENGINEERING QUESTION |
| Rules | Supported ontology constraints or rules | Network rules and validation behavior | ENGINEERING QUESTION |
| Hierarchies | Hierarchy representation | Asset groups, asset types, tiers, subnetworks, and classifications | ENGINEERING QUESTION |
| Spatial meaning | Supported spatial representation | Geometry, topology, proximity, containment, and service areas | ENGINEERING QUESTION |
| Analytics | Semantic model relationship | Supported Esri analytical outputs | VALIDATION REQUIRED |
| Agent grounding | Data Agent grounding model | Esri context exposed to a supported integration | VALIDATION REQUIRED |
| Governance | Ownership, lineage, security, lifecycle | Esri ownership, versioning, licensing, and lifecycle | SOURCE REQUIRED |

## Candidate Progression

```text
Collect source models
    → Classify semantics
    → Validate machine-readable formats
    → Identify candidate correspondences
    → Review with engineering
    → Test a bounded scenario
    → Publish supported architecture
```

No step may be skipped by treating a collection checklist item as evidence.

## Relationship to the Library

| From | To | Relationship |
|---|---|---|
| [03 · ArcGIS Maps for Fabric](../03-ArcGIS-Maps-for-Fabric/) | 04 · Fabric IQ + Spatial Intelligence | Spatial experiences motivate context questions; no product integration is asserted |
| 04 · Fabric IQ + Spatial Intelligence | [05 · Microsoft + Esri Agentic Reference Pattern](../05-Microsoft-Esri-Agentic-Reference-Pattern/) | Validated context could ground agent reasoning in a future reference pattern |
