# Stage 4: Explore and Validate

## Goal

Determine whether the ontology provides correct, useful, attributable spatial business context and whether the customer should continue beyond the proof of concept.

## Validation Views

Use multiple views because no single experience proves the full scenario:

| View | What it validates | Evidence or boundary |
|---|---|---|
| Ontology item | Entity definitions, properties, relationships, and bindings | [IQ-003](records/Evidence.md#iq-003) |
| Ontology agent | Natural-language interpretation and proposal behavior | [IQ-008](records/Evidence.md#iq-008) |
| Optional ontology graph | Relationship-centric exploration | [IQ-007](records/Evidence.md#iq-007) |
| OneLake tables or semantic model | Source values, measures, counts, and lineage | [IQ-002](records/Evidence.md#iq-002) |
| ArcGIS Maps for Fabric or authoritative GIS | Spatial location and relationship review | [IQ-011](records/Evidence.md#iq-011) |

## Tasks

### 1. Run Deterministic Checks

Confirm:

- Entity counts match approved source queries.
- Relationship keys resolve to valid entities.
- Known assets appear in expected service and risk areas.
- Work-order state logic matches business definitions.
- Incident time windows are applied consistently.
- Refresh timestamps and source batches are visible.

### 2. Ask the Test Questions

Example questions:

1. Which critical assets are in high-risk areas?
2. Which of those assets have open high-priority work orders?
3. Which assets are associated with incidents in the last 30 days?
4. Which service areas contain the most affected assets?
5. Why is a selected asset classified as high risk?

For each answer, capture:

- Expected answer
- Actual answer
- Supporting entities and relationships
- Source records
- Reviewer
- Pass, partial, or fail

### 3. Review Spatial Outcomes on a Map

If ArcGIS Maps is in scope:

- Connect it through a documented supported source path.
- Visualize assets, service areas, and risk areas from the governed data.
- Compare sampled spatial relationships with map location.
- Treat the map as a validation and communication view, not proof of a direct ontology integration.

Use [03 · ArcGIS Maps for Fabric](../03-ArcGIS-Maps-for-Fabric/) for map implementation guidance.

### 4. Evaluate Optional Graph Materialization

Materialize a graph only when the POC needs multi-hop relationship exploration. Validate:

- Generated nodes and edges match the ontology.
- Relationship direction and cardinality are understandable.
- Query results can be traced to governed data.
- Graph refresh and lifecycle behavior are acceptable.

Ontology graph support is described in [IQ-007](records/Evidence.md#iq-007). Production lifecycle remains open in [GAP-IQ-003](records/Evidence.md#gap-iq-003).

### 5. Record Production Gaps

At minimum, assess:

- Preview and support constraints
- Capacity and scale
- Refresh and schema evolution
- Binding and graph lifecycle
- Monitoring and lineage
- Identity and access
- Disaster recovery
- Cost and licensing
- Regional availability
- Human review and change control

## Validation Scorecard

| Dimension | Pass condition |
|---|---|
| Business usefulness | The model improves the named operational decision |
| Semantic accuracy | Owners approve entities, properties, and relationships |
| Spatial accuracy | Reviewed relationships match authoritative GIS expectations |
| Data quality | Keys, counts, freshness, and unmatched records meet thresholds |
| Explainability | Answers can be traced to source data and derivation |
| Security | Users see only approved items and data |
| Operability | Refresh, ownership, change, and incident processes are understood |
| Product fit | Preview limits and unresolved gaps are acceptable |

## Decision

Choose one:

- **Continue:** The bounded model is valuable and the remaining gaps are manageable.
- **Revise:** The question is valuable, but data, model, or product gaps require another POC iteration.
- **Stop:** The experience does not justify current preview or operational risk.

## Stage Output

Produce:

- Completed test-question matrix
- Spatial sample-review record
- Ontology and optional graph findings
- Security and lifecycle findings
- Production-gap backlog
- Continue, revise, or stop decision

## Next Pattern

Only after this stage validates trustworthy context should the team use it to inform the [Microsoft + Esri Agentic Reference Pattern](../05-Microsoft-Esri-Agentic-Reference-Pattern/).
