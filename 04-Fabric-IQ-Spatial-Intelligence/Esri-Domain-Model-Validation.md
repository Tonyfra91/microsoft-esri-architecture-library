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
| Product or solution boundary | Utility Network Package Asset Package only; the complete Utility Network information model remains unverified |
| Authoritative model owner | Esri |
| Version or release | Current public ArcGIS Solutions documentation; package schema version remains artifact-specific |
| Machine-readable artifact | Asset Package file geodatabase |
| Mapping status | Partial artifact discovery; candidate mappings are not validated |

## Discovery Status

Esri's [Utility Network Package Asset Package Reference](https://doc.arcgis.com/en/arcgis-solutions/latest/tool-reference/utility-network-package/pdf/Utility%20Network%20Package_Asset%20Package%20Reference.pdf) establishes a technical schema and package artifact. An Asset Package is a file geodatabase that models one utility network's schema, properties, related layers, related tables, and data. Its documented concepts include domain and structure networks, asset groups and asset types, attributes and domains, terminals, categories, network attributes, rules, tiers and subnetworks, associations, controllers, trace configurations, and diagram templates.

This discovery does not establish that the Asset Package is a formal ontology or the complete authoritative Utility Network information model. It provides bounded design-time semantic grounding for candidate Fabric IQ mappings. It does not provide runtime operational data integration, change propagation, or synchronization between ArcGIS and Fabric IQ.

## 1. Information Models

Determine whether Esri publishes an authoritative Utility Network information model and how it differs from industry solution templates or customer implementations.

- [ ] Identify model names, owners, versions, and intended use.
- [ ] Distinguish product semantics from example or industry content.
- [ ] Record licensing and redistribution constraints.

## 2. Schemas

Inventory geodatabase, service, API, configuration, and exchange schemas that encode Utility Network structure.

- [x] Identify an authoritative Asset Package schema reference.
- [x] Determine documented configurable Asset Package elements.
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
- [x] Geodatabase schema exports
- [ ] ArcGIS item or service definitions
- [ ] Other documented formats

## 6. Entity Definitions

Identify authoritative entity concepts such as networks, subnetworks, devices, lines, junctions, structures, associations, and domain-specific assets.

- [ ] Record stable identifiers and labels.
- [x] Identify represented product concepts in the Asset Package.
- [x] Distinguish fixed feature-class roles from customer-configured asset groups and asset types.

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
- [x] Identify the Asset Package table representation for rules.
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

The discovered schema supports bounded candidate mappings for future evaluation. These mappings are hypotheses, not validated semantic equivalence:

| Esri category | Candidate Fabric IQ construct | Status |
|---|---|---|
| Asset group or asset type | Entity type or classification | CANDIDATE ONLY |
| Feature-class field, attribute, or coded domain | Property or controlled value | CANDIDATE ONLY |
| `C_Associations` record | Relationship instance | CANDIDATE ONLY |
| Domain network, tier, subnetwork, or category | Entity, classification, or relationship pattern | CANDIDATE ONLY |
| `B_Rules` row | External constraint or validation metadata | CANDIDATE ONLY |
| Geometry, topology, or trace result | Operational source data or persisted spatial result | CANDIDATE ONLY |

Each candidate requires semantic equivalence analysis, lifecycle analysis, and engineering approval.

The distinction between rules and associations is material. `B_Rules` describes allowed configurations by asset group, asset type, and terminal. `C_Associations` stores actual connectivity, containment, or structural attachment associations between features identified by Global IDs. Neither table alone establishes a Fabric IQ relationship model.

## Application Behavior

Esri's [Apply Asset Package](https://doc.arcgis.com/en/arcgis-solutions/latest/tool-reference/utility-network-package/apply-asset-package.htm) documentation provides implementation guidance:

* Applying schema to an existing configured utility network is additive and does not remove or change existing properties.
* Optional data loading appends feature-class and table data and imports associations and subnetwork controllers.
* Configuration selections apply when `D_Configurations` is present.
* Rename selections apply when `D_Rename` is present.

These behaviors concern Utility Network creation and configuration. They do not establish runtime synchronization with Fabric IQ.

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

## Last Review Date

2026-10-12
