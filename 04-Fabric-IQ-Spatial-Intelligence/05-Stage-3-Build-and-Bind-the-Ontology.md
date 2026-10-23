---
description: Create and bind the bounded Fabric IQ spatial-intelligence ontology.
---

# Stage 3: Build and Bind the Ontology

## Goal

Represent the bounded business model in a Fabric IQ ontology and bind it to the validated entity and relationship data.

For a smaller first exercise using Esri Water Essentials, follow the
[Utility Network ontology quickstart](Quickstart-Utility-Network-Ontology.md).
Its two-entity classification model is an alternative learning path, not an
additional prerequisite for the five-entity MVP below.

## Choose a Creation Path

Ontology supports multiple documented creation approaches:

| Path | Use when | Caution |
|---|---|---|
| Create from scratch | The MVP model is small and the team needs explicit control | Requires deliberate naming and binding |
| Start from a semantic model | A trusted Power BI semantic model already represents the domain | Review generated entities and relationships rather than accepting them automatically |
| Import RDF or OWL | A governed, machine-readable ontology is available | Validate supported constructs and semantic equivalence |

These paths are documented in [IQ-004](records/Evidence.md#iq-004). Esri domain-model import remains unvalidated in [GAP-IQ-005](records/Evidence.md#gap-iq-005).

## Tasks

### 1. Create the Bounded Ontology

Create:

- Asset
- Work order
- Incident
- Service area
- Risk area

Use business language rather than source-system table names.

### 2. Add Properties

For each property:

- Use a clear business definition.
- Identify source and owner.
- Preserve the stable entity key.
- Align data type and null behavior.
- Avoid duplicating properties that differ only by source naming.

### 3. Define Relationships

Create the minimum relationships:

- Asset **has** work order
- Asset **associated with** incident
- Asset **within** service area
- Asset **within** risk area

Use labels that read clearly in both directions. Record whether the relationship is sourced from a business key, an approved spatial derivation, or another governed rule.

### 4. Bind Data

Bind each entity and relationship to the validated Fabric data source. Confirm:

- Key mapping
- Property mapping
- Relationship source and target mapping
- Data visibility for intended users
- Row counts and unmatched keys
- Refresh expectation

The supported ontology concepts and binding behavior are described in [IQ-003](records/Evidence.md#iq-003) and the Microsoft tutorial summarized in [IQ-006](records/Evidence.md#iq-006).

### 5. Add Rules or Metrics Only When Needed

Examples:

- Open work-order count by asset
- Recent incident count by asset
- High-risk-area indicator

Do not reproduce every measure from a semantic model. Add only definitions required to answer and validate the POC question.

### 6. Review the Model

Ask the domain and data owners to verify:

- Entity names and descriptions
- Property meaning
- Relationship direction and cardinality
- Source attribution
- Expected missing or many-to-many cases
- Language used in natural questions

## Use the Ontology Agent Carefully

The ontology agent can assist with creation, binding, questions, and proposal-first changes as documented in [IQ-008](records/Evidence.md#iq-008).

For the POC:

- Review every proposed model change before applying it.
- Compare answers with the expected-answer set.
- Treat generated explanations as untrusted until verified.
- Do not grant action-taking authority.

## Stage Output

Produce:

- Bound ontology
- Entity and relationship definitions
- Binding map
- Data-owner approval
- Unmatched-key and data-quality report
- List of deferred properties, rules, metrics, and entities

## Exit Gate

Proceed only if:

- Every entity and relationship maps to an approved source.
- Stable keys produce expected row and relationship counts.
- Business owners approve the vocabulary.
- Known test cases can be located and explained.
- No direct Esri integration is implied without evidence.
