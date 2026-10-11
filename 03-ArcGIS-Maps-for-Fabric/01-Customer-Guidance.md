# ArcGIS Maps for Microsoft Fabric: Customer Guidance

## Executive Summary

ArcGIS Maps for Microsoft Fabric provides a map-authoring experience inside Microsoft Fabric. A successful proof of concept requires administrative enablement, qualifying roles in both Fabric and ArcGIS Online, supported source data, a bounded map question, and explicit validation of production gaps.

## Where the Component Fits

Maps for Fabric is the spatial-experience area in the library progression:

```text
Data → Spatial Processing → Spatial Experience
```

This component should not be positioned as a replacement for GeoAnalytics, ArcGIS for Power BI, or operational ArcGIS applications.

## Foundational Requirements

| Area | Requirement | Evidence |
|---|---|---|
| Fabric tenant | Tenant administrator enables the workload | MAP-002 |
| Capacity | Workspace capacity is sufficient to save workload items; minimum SKU is not published | MAP-002; GAP-001 |
| Workspace | A Fabric workspace and item location are selected | MAP-004 |
| ArcGIS account | Organizational account required; Public accounts are unsupported | MAP-003 |
| Map author | ArcGIS Creator or higher and Fabric Contributor or higher | MAP-003 |
| Map viewer | ArcGIS Viewer or higher and Fabric Viewer or higher | MAP-003 |
| Data | Supported lakehouse, ArcGIS Online, or Living Atlas source | MAP-005 |

See [Stage 1](03-Stage-1-Enable-and-Authorize.md) for required API permissions and the implementation sequence.

## Customer Discovery

### Business outcome

- [ ] What decision or analytical question requires a map?
- [ ] Who will use the map, and in which Fabric experience?
- [ ] What measurable result will make the proof of concept successful?

### Data readiness

- [ ] Which Fabric data item is authoritative?
- [ ] Which fields contain coordinates, geometry, addresses, or other location information?
- [ ] What is the coordinate system?
- [ ] What volume, refresh frequency, and latency are required?
- [ ] Is every proposed input documented as supported?

### Identity and access

- [ ] Which Microsoft identity and Fabric role does each user have?
- [ ] Is an ArcGIS identity or license required for the selected capability?
- [ ] Who may create, save, share, and view the map?
- [ ] Which tenant, capacity, or workspace administrators must participate?

### Security and governance

- [ ] Does customer data cross a Microsoft, customer, or Esri boundary?
- [ ] Which endpoints and protocols are required?
- [ ] Are private networking or outbound restrictions in scope?
- [ ] How are saved maps, shared content, and derived outputs governed?

### Production readiness

- [ ] Does the customer require a documented network allow list?
- [ ] What refresh and caching behavior must be validated?
- [ ] Which audit and telemetry records are required?
- [ ] Which geography and data-residency requirements apply?
- [ ] What sharing behavior must be supported beyond saving and opening the item?

## Proof-of-Concept Framework

A bounded proof of concept should identify:

1. A business question that requires spatial visualization.
2. One supported Fabric data source.
3. Documented location fields or geometry.
4. One supported Maps for Fabric workflow.
5. A named audience and access model.
6. A documented save or sharing outcome, if required.
7. Measurable success criteria.

## Recommended POC Stages

| Stage | Owner focus | Outcome |
|---|---|---|
| 1. Enable and authorize | Tenant, Fabric, and ArcGIS administrators | Enabled workload and valid pilot roles |
| 2. Prepare and connect data | Data owner and map author | Supported, approved map layers |
| 3. Build and style the map | Map author and business reviewer | Usable map item |
| 4. Validate and operationalize | Platform, security, and business owners | Validated outcome and production gap list |

Follow the [End-to-End Scenario](02-End-to-End-Scenario.md) for implementation detail.

## Minimum POC Exit Criteria

- [ ] The workload is enabled through an approved administrative process.
- [ ] The selected data belongs to a documented supported category.
- [ ] Required Microsoft and ArcGIS identities and roles are validated.
- [ ] The author can create, save, and reopen the map.
- [ ] The intended viewer can access and interact with the map.
- [ ] The map answers a measurable business question.
- [ ] Network, refresh, telemetry, residency, capacity, and sharing gaps have owners.

## Scope and Boundaries

This guide does not prescribe:

- A production deployment architecture.
- A network allow list.
- A data residency or telemetry statement.
- An integration with Fabric IQ or agentic systems.
- A minimum Fabric capacity SKU.
- A complete publishing or sharing mechanism beyond documented save and open behavior.

## Supporting Technical Records

- [Architecture](Architecture.md)
- [Architecture mapping](Architecture-Mapping.md)
- [End-to-end scenario](02-End-to-End-Scenario.md)
- [Evidence register](records/Evidence.md)
- [Source register](records/Source-Register.md)
- [Collection checklist](records/Collection-Checklist.md)
- [Public research](records/Public-Research.md)
