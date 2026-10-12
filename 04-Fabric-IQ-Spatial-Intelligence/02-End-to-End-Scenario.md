# Fabric IQ Spatial Intelligence End-to-End Scenario

## Scenario at a Glance

### Example POC Question

> Which operational assets are located within high-risk service areas, have open work orders, and are associated with recent incidents?

The scenario creates a bounded business model over governed data. GeoAnalytics computes the required spatial facts, ontology binds those facts to business entities and relationships, and users validate the results through structured exploration, optional graph views, ontology-agent questions, and a parallel map view.

```mermaid
flowchart LR
    S1["Stage 1<br/>Establish the foundation"]
    S2["Stage 2<br/>Prepare entities and relationships"]
    S3["Stage 3<br/>Build and bind the ontology"]
    S4["Stage 4<br/>Explore and validate"]

    S1 --> S2 --> S3 --> S4
```

## Why Four Stages

| Stage | Decision it proves | Primary output |
|---|---|---|
| 1. Establish the foundation | Can the customer safely run the preview POC? | Approved workspace, access, scope, owners, and test plan |
| 2. Prepare entities and relationships | Can authoritative data answer the spatial business question? | Governed entity and relationship tables |
| 3. Build and bind the ontology | Can the bounded business model be represented and connected to data? | Bound ontology with validated keys and relationships |
| 4. Explore and validate | Does the experience produce correct and useful business context? | Evidence-backed POC decision and operational backlog |

## End-to-End Flow

```mermaid
flowchart TB
    A["Authoritative asset, work-order,<br/>incident, boundary, and risk data"]
    B["Standardize keys, timestamps,<br/>ownership, and geometry"]
    C["GeoAnalytics derives only the<br/>required spatial relationships"]
    D[("OneLake<br/>Entity and relationship tables")]
    E["Fabric IQ ontology (preview)<br/>Define and bind business meaning"]
    F["Optional graph materialization<br/>and ontology agent"]
    G["ArcGIS Maps for Fabric<br/>Visualize the governed data"]
    H["Business and data owners<br/>Validate expected outcomes"]

    A --> B --> C --> D --> E --> F --> H
    D --> G --> H
```

## Reference Data Model

```mermaid
erDiagram
    ASSET ||--o{ WORK_ORDER : "has"
    ASSET }o--o{ INCIDENT : "associated with"
    SERVICE_AREA ||--o{ ASSET : "contains"
    RISK_AREA }o--o{ ASSET : "contains"
    SERVICE_AREA }o--o{ RISK_AREA : "overlaps"

    ASSET {
        string asset_id PK
        string name
        string asset_type
        string status
        string criticality
    }
    WORK_ORDER {
        string work_order_id PK
        string asset_id FK
        string priority
        string state
        datetime due_date
    }
    INCIDENT {
        string incident_id PK
        string category
        string severity
        datetime occurred_at
    }
    SERVICE_AREA {
        string service_area_id PK
        string name
        string owner
        string service_level
    }
    RISK_AREA {
        string risk_area_id PK
        string risk_type
        string rating
        date effective_from
        date effective_to
    }
```

The physical implementation can use separate relationship tables even when the conceptual diagram shows direct associations.

## Scenario Outputs

| Output | Description |
|---|---|
| Entity contract | Keys, names, properties, owners, sources, and freshness expectations |
| Relationship contract | Source and target keys, semantics, derivation method, lineage, and refresh |
| Governed OneLake tables | Testable entity and relationship records |
| Bound ontology | Bounded business model connected to governed data |
| Validation pack | Test questions, expected answers, sampled relationship checks, and findings |
| Decision record | Continue, revise, or stop, with preview and production gaps |

## Required Evidence

The scenario relies on:

- Ontology entities, relationships, and bindings: [IQ-003](records/Evidence.md#iq-003)
- Ontology creation paths: [IQ-004](records/Evidence.md#iq-004)
- Tenant requirements: [IQ-005](records/Evidence.md#iq-005)
- Tutorial behavior: [IQ-006](records/Evidence.md#iq-006)
- Optional graph exploration: [IQ-007](records/Evidence.md#iq-007)
- Optional ontology-agent experience: [IQ-008](records/Evidence.md#iq-008)
- Repository spatial-preparation boundary: [IQ-010](records/Evidence.md#iq-010)
- Separate ArcGIS Maps path: [IQ-011](records/Evidence.md#iq-011)

## Stage Sequence

1. [Stage 1: Establish the Foundation](03-Stage-1-Establish-the-Foundation.md)
2. [Stage 2: Prepare Entities and Relationships](04-Stage-2-Prepare-Entities-and-Relationships.md)
3. [Stage 3: Build and Bind the Ontology](05-Stage-3-Build-and-Bind-the-Ontology.md)
4. [Stage 4: Explore and Validate](06-Stage-4-Explore-and-Validate.md)
