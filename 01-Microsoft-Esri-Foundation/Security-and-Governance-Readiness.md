---
description: Customer readiness decisions for identity, data protection, network boundaries, credentials, audit, and approval across Microsoft and Esri workloads.
ms.date: 2026-10-23
ms.topic: how-to
---

# Security and Governance Readiness

Before connecting business and geospatial data, agree on who can access it,
how sensitive information is protected, which connections are permitted, and
how activity will be monitored. Review Microsoft and Esri controls together:
securing Fabric alone does not establish a secured end-to-end experience.

Use this checklist with the customer's Fabric administrator, ArcGIS
administrator, data owner, and security or governance team before following a
component walkthrough. It is preparation guidance, not a security certification,
compliance assessment, or claim that every integration supports every control.

[Return to the Foundation introduction](README.md)

## Start with Controls, Not a Product Shopping List

Use existing customer controls and operating processes where they satisfy the
workload's requirements. Microsoft Purview and Microsoft Sentinel can support
the design; neither is a universal prerequisite for every POC.

For a sample-data exercise, agree a limited scope and document why any control
is not applicable. Before using sensitive or production data, revalidate the
scope, controls, licensing, support, and operational ownership. Sample data does
not remove the need to protect identities, credentials, and shared resources.

## Six Decisions Before Connecting Data

### 1. Identity and Access

- Identify interactive users, administrators, and workload identities separately.
  Apply least-privilege Fabric and ArcGIS roles, with approved MFA and
  Conditional Access policies for interactive access where supported.
- Document who may read, author, share, export, administer, or write back.
  Check source-data permissions as well as workspace, item, and application access.
- Test an approved user and an unauthorized test identity against the selected
  data and output. Do not assume an Entra sign-in automatically grants or
  propagates ArcGIS authorization. Assign an owner for access review and removal.

Use the [Fabric security overview](https://learn.microsoft.com/en-us/fabric/security/security-overview)
and the ArcGIS security guidance in [Authoritative References](#authoritative-references).

### 2. Data Protection and Governance

- Name data owners and classify inputs, intermediate data, outputs, and logs.
  Include sensitive infrastructure locations, customer locations, network
  relationships, and location-derived information, not only personal data.
- Agree sharing, export, retention, deletion, and residency requirements.
  Review licensing and permitted use of ArcGIS, Living Atlas, and sample content.
- Determine which native Fabric governance features and applicable Purview
  protections are needed. Validate coverage for the selected item types and
  data paths; test intended sharing and export restrictions.

Do not assume labels, policies, lineage, or permissions automatically follow
data copied between ArcGIS, OneLake, reports, files, ontology, and agent tools.
Derived results and exported files need their own classification and access review.

### 3. Network Boundaries

- Inventory connections between customer systems, Fabric, ArcGIS, and any
  external services. Record purpose, direction, protocol, authentication,
  endpoint requirements, and the data or telemetry crossing each boundary.
- Separate inbound access controls from outbound access restrictions. Validate
  Private Link, managed networking, firewall, proxy, and egress requirements
  against the specific workload rather than assuming platform-wide compatibility.
- Have the network and security owners approve and test the required paths.
  Record unsupported combinations and unresolved endpoint or residency questions.

> [!WARNING]
> GeoAnalytics is currently unsupported when Outbound Access Protection is
> enabled. It needs outbound Esri communication for authorization and usage
> reporting. Follow the [GeoAnalytics network-readiness discovery](../02-GeoAnalytics-for-Fabric/01-Customer-Guidance.md#network-readiness-discovery)
> and its [evidence](../02-GeoAnalytics-for-Fabric/records/Evidence.md#sec-004).
> If a mandatory customer control conflicts with the workload, stop and resolve
> the design with the security owner and product teams. Do not disable required
> controls merely to make a demonstration run.

### 4. Credentials and Secrets

- Use an approved secret store and supported retrieval mechanism. Do not put
  passwords, API keys, tokens, or credential files in source control, shared
  notebooks, screenshots, or logs.
- Record the credential's purpose, scope, owner, expiry, rotation, and revocation
  process. Use workload identities where the selected integration supports them;
  do not assume every Esri authorization path accepts an Entra workload identity.
- Verify that secrets are not exposed in outputs or error messages. For
  GeoAnalytics, see the documented
  [Key Vault and credential guidance](../02-GeoAnalytics-for-Fabric/records/Evidence.md#sec-003).

### 5. Audit, Detection, and Response

- Agree which sign-in, administrative, data-access, sharing, export, and
  workload activities require records. Identify what each product actually
  emits; document coverage gaps rather than assuming every action is logged.
- Define log collection, retention, access, residency, expected collection
  delay, and investigation ownership. Logs can contain sensitive information too.
- Generate approved test activity and confirm the expected records arrive.
  If alerts or SIEM integration are required, test the supported ingestion path,
  the selected detection, and the analyst's response procedure.

Fabric activity audit, ArcGIS operational logs, and identity logs are different
sources. Availability, licensing, and collection mechanisms vary. Microsoft
Sentinel or another customer-approved SIEM needs an explicitly configured and
validated collection path; enabling it does not automatically collect all
Fabric or ArcGIS activity.

### 6. Readiness Approval and Ownership

- Assign a decision owner for data use, access, network policy, monitoring,
  credentials, and the selected application or workload.
- Record tested controls, unresolved risks, approved exceptions, expiry dates,
  and the permitted POC scope. Required controls that cannot be met are blockers,
  not successful readiness checks.
- Obtain the customer's approval before connecting the agreed data. Revisit
  readiness when moving to production, changing sources or identities, adding
  write operations, or introducing ontology, graph, or agent experiences.

Human approval for an agent action does not replace authorization, data
protection, logging, or validation of the tool performing that action.

## Where Purview and Sentinel Fit

| Capability             | Customer purpose                                                   | Boundary to validate                                                              |
|------------------------|--------------------------------------------------------------------|-----------------------------------------------------------------------------------|
| Native Fabric controls | Govern workspace, item, and data access; discover and govern data    | Configure permissions and applicable OneLake catalog features for the workload     |
| ArcGIS controls        | Govern ArcGIS identities, roles, content sharing, and service access | Review ArcGIS Online settings or the customer's ArcGIS Enterprise deployment       |
| Microsoft Purview      | Add applicable information protection, DLP, audit, and compliance   | Confirm item and data-path coverage, licensing, policy configuration, and behavior  |
| Microsoft Sentinel     | Collect selected security signals for detection and investigation   | Confirm supported connectors or ingestion, retention, detections, and SOC ownership |

Fabric's OneLake catalog remains its primary native governance experience.
[Purview adds protection, audit, risk, and compliance capabilities](https://learn.microsoft.com/en-us/fabric/governance/microsoft-purview-fabric);
it is not a replacement for source permissions or a guarantee that every export
or Esri artifact inherits protection.

[Sentinel data connectors](https://learn.microsoft.com/en-us/azure/sentinel/connect-data-sources)
provide supported collection options. Do not assume a native connector exists
for every ArcGIS or Fabric event source. Use the customer's existing SIEM if
appropriate, and verify the actual event source and supported collection route.

## Minimum Readiness Record

Keep the record in the customer's approved governance location, not this public
repository. Record the following for each applicable area:

| Record field    | What to capture                                                     |
|-----------------|---------------------------------------------------------------------|
| Scope           | Workload, environment, approved data, users, and intended operations  |
| Requirement     | Customer policy or risk being addressed; rationale if not applicable |
| Implementation  | Selected control, configuration, and supporting product guidance     |
| Evidence        | Test identity or activity, expected result, observed result, and date |
| Accountability  | Owner, reviewer, and approval decision                               |
| Open conditions | Gap or exception, risk decision, expiry, and required follow-up      |

- [ ] Data owners approve the sources, derived outputs, and permitted use.
- [ ] Access tests confirm both intended access and denial for unauthorized users.
- [ ] Required network paths work without violating mandatory customer controls.
- [ ] Credentials are stored, retrieved, and managed through approved mechanisms.
- [ ] Required audit records and any agreed alerting or SIEM path have been tested.
- [ ] No required control remains unmet; applicable exceptions have explicit approval.
- [ ] Customer owners approve the recorded scope before data is connected.

## Continue with the Selected Workload

- [GeoAnalytics readiness and network discovery](../02-GeoAnalytics-for-Fabric/01-Customer-Guidance.md#what-you-need-to-run-geoanalytics)
- [Maps for Fabric requirements and discovery](../03-ArcGIS-Maps-for-Fabric/01-Customer-Guidance.md#foundational-requirements)
- [Fabric IQ foundational requirements](../04-Fabric-IQ-Spatial-Intelligence/01-Customer-Guidance.md#minimum-foundational-requirements)
- [Water Essentials ontology quickstart prerequisites](../04-Fabric-IQ-Spatial-Intelligence/Quickstart-Utility-Network-Ontology.md#before-you-start)
- [Conceptual agentic security and governance validation](../05-Microsoft-Esri-Agentic-Reference-Pattern/README.md#identity-security-and-governance-validation)

The component guidance owns product-specific requirements and evidence gaps.
This shared checklist does not establish a native Esri-to-Fabric-IQ integration,
an end-to-end monitoring solution, or production support for preview features.

## Authoritative References

Reviewed 2026-10-23. Product capabilities below support the preparation guidance;
customer-specific configurations and effectiveness still require validation.

- [Security in Microsoft Fabric](https://learn.microsoft.com/en-us/fabric/security/security-overview):
  identity, authorization, network security, and platform controls
- [Use Microsoft Purview with Microsoft Fabric](https://learn.microsoft.com/en-us/fabric/governance/microsoft-purview-fabric):
  native Fabric governance versus Purview protection, audit, and compliance
- [Microsoft Sentinel data connectors](https://learn.microsoft.com/en-us/azure/sentinel/connect-data-sources):
  supported collection mechanisms and data-management considerations
- [ArcGIS Online security configuration](https://doc.arcgis.com/en/arcgis-online/administer/configure-security.htm):
  organization access, sharing, sign-in, and security settings
- [ArcGIS Enterprise security best practices](https://doc.esri.com/en/arcgis-enterprise/latest/plan/security-best-practices.html):
  deployment-specific controls, HTTPS, certificates, and access
- [GeoAnalytics security evidence](../02-GeoAnalytics-for-Fabric/records/Evidence.md#sec-001):
  authorization, credential handling, outbound calls, and unresolved network questions
