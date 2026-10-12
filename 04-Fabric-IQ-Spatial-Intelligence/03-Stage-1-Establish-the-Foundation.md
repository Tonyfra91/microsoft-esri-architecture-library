# Stage 1: Establish the Foundation

## Goal

Approve a bounded preview proof of concept before creating ontology artifacts or processing production data.

## Entry Conditions

- A customer decision or operational question is named.
- A business sponsor and technical owner are available.
- Candidate data sources can be assessed.
- Preview evaluation is permitted in principle.

## Tasks

### 1. Confirm the POC Question

Use the reference question or substitute one question of comparable scope:

> Which operational assets are located within high-risk service areas, have open work orders, and are associated with recent incidents?

Define:

- Intended user
- Decision the answer supports
- Expected answer format
- Maximum acceptable data age
- Known examples for validation

### 2. Approve the Preview Boundary

Record:

- Business data classification allowed in the POC
- Approved region and Fabric capacity
- Preview support expectations
- Whether ontology agent and graph materialization are approved
- Whether ArcGIS Maps will be included as a separate validation view

Ontology and its tenant settings are documented as preview capabilities in [IQ-003](records/Evidence.md#iq-003) and [IQ-005](records/Evidence.md#iq-005).

### 3. Establish the Workspace

Verify:

- Fabric capacity is available.
- The selected workspace is governed and access-controlled.
- POC users can create Fabric items.
- POC users can create ontology preview items.
- Users can read every source intended for binding.
- Separate permissions for optional graph, ontology-agent, and ArcGIS experiences are understood.

### 4. Assign Ownership

| Role | Minimum responsibility |
|---|---|
| Business sponsor | Approve question, expected value, and continuation decision |
| Domain owner | Approve entity definitions and relationship meaning |
| Data owner | Approve source, keys, quality, access, and refresh |
| Spatial analyst | Approve geometry, spatial method, and sampled relationships |
| Fabric owner | Configure workspace, capacity, bindings, and lifecycle |
| ArcGIS owner | Approve any ArcGIS source or map experience |
| Security or governance reviewer | Approve preview use, access, and data classification |

### 5. Define Acceptance Tests

Create a small validation set before implementation:

- Five to ten assets with known service areas
- Assets known to be inside and outside risk areas
- Open and closed work-order examples
- Recent and historical incident examples
- At least five natural-language test questions
- Expected answers and authoritative reviewers

## Stage Output

Produce:

- Approved POC charter
- Named workspace and owners
- Preview approval record
- Source inventory
- Test-question and expected-answer set
- Initial risk and gap log

## Exit Gate

Proceed only if:

- Required tenant settings can be enabled.
- Source access is approved.
- Stable candidate entity keys exist.
- The customer accepts preview limitations.
- Expected answers can be independently reviewed.

Otherwise, stop and resolve the missing foundation before building the ontology.
