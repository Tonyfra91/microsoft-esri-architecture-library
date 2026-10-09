# Esri Domain Model Validation

## Purpose

This engineering discovery document identifies where authoritative Esri domain semantics are encoded and whether they are available in machine-readable form. Utility Network is the first candidate domain.

> **ENGINEERING QUESTION**
>
> For Utility Network and other Esri domains, where is the authoritative domain model encoded today? Does Esri have information models, schemas, knowledge graph models, formal ontologies, or some combination, and are those definitions and relationships available in a machine-readable form?

## Candidate Domain

| Field | Initial value |
|---|---|
| Domain | Utility Network |
| Product or solution boundary | VALIDATION REQUIRED |
| Authoritative model owner | ENGINEERING QUESTION |
| Version or release | SOURCE REQUIRED |
| Machine-readable artifact | ENGINEERING QUESTION |
| Mapping status | Not started |

## 1. Information Models

Determine whether Esri publishes an authoritative Utility Network information model and how it differs from industry solution templates or customer implementations.

- [ ] Identify model names, owners, versions, and intended use.
- [ ] Distinguish product semantics from example or industry content.
- [ ] Record licensing and redistribution constraints.

## 2. Schemas

Inventory geodatabase, service, API, configuration, and exchange schemas that encode Utility Network structure.

- [ ] Identify authoritative schema definitions.
- [ ] Determine which schema elements are configurable.
- [ ] Record versioning and compatibility rules.

## 3. Knowledge Graph Models

Determine whether Utility Network concepts are represented in ArcGIS Knowledge or another Esri graph model.

- [ ] Identify graph schemas or entity-relation models.
- [ ] Distinguish operational network topology from knowledge graph semantics.
- [ ] Record supported export or query mechanisms.

## 4. Formal Ontologies

Determine whether Esri publishes a formal ontology for Utility Network or related industry domains.

- [ ] Search for RDF, OWL, SHACL, SKOS, or equivalent artifacts.
- [ ] Identify governance, ownership, and versioning.
- [ ] Confirm whether any artifact is normative or illustrative.

## 5. Machine-Readable Formats

Identify supported formats for consuming definitions and relationships programmatically.

- [ ] JSON or JSON Schema
- [ ] XML or XML Schema
- [ ] OpenAPI or service metadata
- [ ] RDF, OWL, SHACL, or SKOS
- [ ] Geodatabase schema exports
- [ ] ArcGIS item or service definitions
- [ ] Other documented formats

## 6. Entity Definitions

Identify authoritative entity concepts such as networks, subnetworks, devices, lines, junctions, structures, associations, and domain-specific assets.

- [ ] Record stable identifiers and labels.
- [ ] Identify abstract and concrete entity types.
- [ ] Distinguish product entities from customer-configured asset types.

## 7. Properties

Identify required, optional, derived, and customer-defined properties.

- [ ] Record data types, units, domains, and nullability.
- [ ] Identify authoritative definitions and default values.
- [ ] Distinguish stored values from computed state.

## 8. Relationships

Identify connectivity, containment, structural attachment, association, ownership, and other domain relationships.

- [ ] Record relationship direction and cardinality.
- [ ] Identify whether relationships are stored, computed, or inferred.
- [ ] Identify lifecycle and validation behavior.

## 9. Rules

Identify network rules, attribute rules, validation rules, and other constraints.

- [ ] Record rule ownership and execution context.
- [ ] Identify machine-readable representations.
- [ ] Distinguish normative product rules from customer configuration.

## 10. Hierarchies

Identify asset groups, asset types, tiers, subnetworks, categories, and other classification or containment hierarchies.

- [ ] Record hierarchy semantics and identifiers.
- [ ] Identify configurable versus fixed structures.
- [ ] Determine how hierarchy changes are versioned.

## 11. Geographic and Spatial Relationships

Identify geometry, topology, spatial reference, containment, adjacency, proximity, service-area, and network-trace semantics.

- [ ] Distinguish geometry from network topology.
- [ ] Identify relationships that must be computed at query time.
- [ ] Record precision, coordinate-system, and scale considerations.

## 12. Candidate Fabric IQ Mappings

Do not perform mappings in this phase.

For future evaluation, record only potential mapping categories:

| Esri category | Candidate Fabric IQ construct | Status |
|---|---|---|
| Entity definition | Entity type | NOT MAPPED |
| Property | Property | NOT MAPPED |
| Domain relationship | Relationship | NOT MAPPED |
| Hierarchy | Hierarchy or relationship pattern | NOT MAPPED |
| Rule | Constraint or external validation | NOT MAPPED |
| Spatial relationship | Stored relation or spatial tool result | NOT MAPPED |

Each candidate requires semantic equivalence analysis, lifecycle analysis, and engineering approval.

## 13. Unknowns Requiring Esri Engineering Validation

- [ ] Which Utility Network artifact is the authoritative domain definition?
- [ ] Which semantics exist only in product code or service behavior?
- [ ] Which definitions are exposed through supported APIs?
- [ ] Which artifacts are stable and versioned for external consumption?
- [ ] Which industry models are normative, recommended, or illustrative?
- [ ] Does Esri publish any formal ontology for Utility Network?
- [ ] Can relationship and rule definitions be exported in machine-readable form?
- [ ] Which terms may be reused in an external ontology or semantic model?
- [ ] How should customer extensions be represented?
- [ ] Which spatial relationships must remain dynamic computations?

## Discovery Output

The discovery phase should produce:

1. A source inventory with owners and versions.
2. An artifact classification by model type.
3. A machine-readable format inventory.
4. A list of authoritative and non-authoritative semantics.
5. Engineering answers to the open questions.
6. A recommendation on whether candidate mapping should proceed.
