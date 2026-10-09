# Fabric IQ + Spatial Intelligence Architecture

## Purpose

This document defines the architecture exploration boundary for bringing spatial and Esri domain context into Fabric IQ discussions.

## Architectural Position

The library narrative places this area after spatial processing and spatial experience:

```text
Data → Spatial Processing → Spatial Experience → Context
```

The word *context* describes the investigation goal. It does not assert an implemented integration.

## Candidate Context Layers

| Layer | Candidate role | Status |
|---|---|---|
| Fabric data | Authoritative business and analytical data | SOURCE REQUIRED |
| Semantic models | Measures, dimensions, and analytical meaning | SOURCE REQUIRED |
| Fabric IQ ontology | Business entities and relationships | VALIDATION REQUIRED |
| Graph | Traversable relationships among grounded entities | VALIDATION REQUIRED |
| Data Agents | Conversational access to supported grounded data | VALIDATION REQUIRED |
| Esri domain context | Domain entities, properties, rules, and hierarchies | ENGINEERING QUESTION |
| Spatial context | Geometry and geographic relationships | ENGINEERING QUESTION |

## Architecture Boundary

No connection between an Esri artifact and Fabric IQ is treated as supported until:

1. The Esri source model is identified and authoritative.
2. The Fabric IQ target construct is documented.
3. Machine-readable exchange or integration is technically possible.
4. Identity, security, governance, and lifecycle behavior are understood.
5. Microsoft and Esri engineering validate the interpretation.

## Architecture Questions

1. What does Fabric IQ treat as an entity, property, relationship, rule, and hierarchy?
2. How do semantic models and ontology artifacts relate?
3. Which graph capabilities are available and how are they governed?
4. What grounding does a Data Agent consume?
5. Where are Esri domain definitions encoded and versioned?
6. Which spatial relationships must remain computed rather than modeled?
7. How would updates, lineage, ownership, and semantic conflicts be managed?
8. Which identity and authorization context applies at query time?

## Prohibited Assumptions

This architecture must not assume:

- Esri provides a Fabric IQ ontology.
- Utility Network is a formal ontology.
- ArcGIS Knowledge Graph and Fabric IQ graph concepts are equivalent.
- A geodatabase schema captures all domain semantics.
- Spatial relationships should be materialized as static graph edges.
- Data Agents can invoke ArcGIS or spatial tools without a supported integration.

## Planned Architecture Views

| View | Status | Evidence gate |
|---|---|---|
| Fabric IQ context model | SOURCE REQUIRED | Current Microsoft architecture documentation |
| Esri domain model inventory | ENGINEERING QUESTION | Utility Network artifact collection |
| Candidate semantic alignment | NOT STARTED | Both source and target models validated |
| Identity and governance | VALIDATION REQUIRED | Microsoft and Esri security documentation |
| Bounded proof of concept | NOT STARTED | Approved candidate mapping and scenario |

## Validation Status

Exploration Only
