# ArcGIS Maps for Microsoft Fabric Architecture

## Purpose

This architecture record defines what must be validated before publishing a component or deployment architecture for ArcGIS Maps for Microsoft Fabric.

## Architectural Position

ArcGIS Maps for Microsoft Fabric is positioned in this library as the spatial experience that follows data preparation and spatial processing:

```text
Supported Fabric data → Mapping and exploration experience → Customer insight
```

This sequence is a library narrative, not a technical data-flow claim.

## Candidate Component Boundary

The following elements require validation before they are connected in an architecture diagram:

| Candidate element | Validation needed |
|---|---|
| Microsoft Fabric workspace | Capacity, workspace, region, and permission requirements |
| ArcGIS Maps for Microsoft Fabric workload | Installation, enablement, lifecycle, and runtime boundary |
| Supported Fabric data | Supported item types, formats, geometry, location fields, and query behavior |
| ArcGIS services | Required services, optional services, endpoints, and data exchange |
| User identity | Fabric identity, ArcGIS identity, licensing, roles, and sign-in behavior |
| Map output | Save, share, refresh, export, and downstream consumption behavior |

> **VALIDATION REQUIRED**
>
> Do not draw arrows between these elements until the corresponding data flow and boundary crossing are supported by authoritative evidence.

## Architecture Questions

1. Where does the Maps for Fabric workload execute?
2. Which Fabric capacities, workspaces, and regions support it?
3. Which Fabric data items and location representations are supported?
4. Does the product copy, cache, query, or otherwise transmit customer data?
5. Which ArcGIS services are contacted, under what conditions, and for what purpose?
6. Which Microsoft and Esri identities, licenses, and roles are required?
7. How are maps saved, shared, refreshed, and governed?
8. Which tenant, capacity, or workspace controls apply?
9. What limitations affect production deployment?

## Candidate Architecture Views

| View | Status | Evidence gate |
|---|---|---|
| Product component view | VALIDATION REQUIRED | Product boundary and required components |
| Data-flow view | VALIDATION REQUIRED | Supported inputs, query/copy behavior, and outputs |
| Identity and authorization view | VALIDATION REQUIRED | Microsoft and Esri identity documentation |
| Network and trust-boundary view | VALIDATION REQUIRED | Endpoints, protocols, and data handling |
| Minimum POC view | VALIDATION REQUIRED | Confirmed prerequisites and bounded customer scenario |

## Dependencies

> **SOURCE REQUIRED**
>
> Required and optional dependencies have not been promoted into this architecture. Collect current product, administration, licensing, and deployment documentation first.

## Validation Status

Architecture Validation Required
