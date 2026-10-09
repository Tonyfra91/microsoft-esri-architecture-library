# ArcGIS Maps for Microsoft Fabric: Customer Guidance

## Executive Summary

ArcGIS Maps for Microsoft Fabric should be introduced through a bounded customer question and a documented product path. This guide captures discovery questions and proof-of-concept criteria while the product architecture is validated.

## Where the Component Fits

Maps for Fabric is the spatial-experience area in the library progression:

```text
Data → Spatial Processing → Spatial Experience
```

This component should not be positioned as a replacement for GeoAnalytics, ArcGIS for Power BI, or operational ArcGIS applications.

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

> **VALIDATION REQUIRED**
>
> The questions above identify information to collect. They do not imply a particular identity, network, or data-flow implementation.

## Proof-of-Concept Framework

A bounded proof of concept should identify:

1. A business question that requires spatial visualization.
2. One supported Fabric data source.
3. Documented location fields or geometry.
4. One supported Maps for Fabric workflow.
5. A named audience and access model.
6. A documented save or sharing outcome, if required.
7. Measurable success criteria.

## Minimum POC Exit Criteria

- [ ] Product prerequisites are supported by authoritative sources.
- [ ] The selected data item and location representation are supported.
- [ ] Required identities, licenses, and roles are documented.
- [ ] The intended audience can access the map.
- [ ] Refresh and sharing behavior are tested.
- [ ] Network and data-handling assumptions are recorded.
- [ ] Open limitations are accepted by the customer.

## Scope and Boundaries

Until the evidence register is populated, this guide does not prescribe:

- A production deployment architecture.
- A specific authentication flow.
- A supported list of data sources or formats.
- A network allow list.
- A data residency or telemetry statement.
- An integration with Fabric IQ or agentic systems.

## Supporting Technical Records

- [Architecture](Architecture.md)
- [Architecture mapping](Architecture-Mapping.md)
- [Evidence register](records/Evidence.md)
- [Source register](records/Source-Register.md)
- [Collection checklist](records/Collection-Checklist.md)
