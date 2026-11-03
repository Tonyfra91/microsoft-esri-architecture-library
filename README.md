---
description: "Customer and partner architecture guidance for Microsoft Fabric and Esri, with documented product paths, preview patterns, and bounded experiments."
---

# Microsoft + Esri Architecture Library

Architecture guidance, customer walkthroughs, and technical experiments for
combining Microsoft Fabric's data and analytics capabilities with Esri's
geospatial capabilities.

## Purpose

This repository helps customers and partners understand where Microsoft Fabric
and Esri fit together, what is required to use them, and which architecture
decisions still need validation. It connects the introductory story to customer
discovery, implementation stages, diagrams, and supporting technical evidence.

The library addresses three related questions:

* How can ArcGIS GeoAnalytics process and enrich spatial data in Fabric Spark?
* How can ArcGIS Maps help people visualize and explore supported data in Fabric?
* How might Esri spatial relationships and domain models provide business context
  for Fabric IQ ontologies and future agentic scenarios?

The first two areas cover documented product capabilities. Ontology and agentic
areas have different maturity levels: preview patterns, conceptual proposals,
and experiments are labeled rather than presented as completed integrations.

## Who This Is For

* Customers and partners assessing Microsoft + Esri scenarios and planning a
  bounded proof of concept
* Solution architects and technical sellers framing the customer journey,
  dependencies, and architecture boundaries
* Fabric engineers and GIS practitioners working through setup, data preparation,
  spatial processing, mapping, and validation
* Platform and governance owners reviewing capacity, identity, access, networking,
  and preview readiness

## What You Will Find

* Customer guidance and discovery questions to establish fit and scope
* End-to-end scenarios and stage-by-stage walkthroughs where available
* Architecture diagrams explaining components, data paths, and boundaries
* Evidence and source registers linking technical claims to Microsoft and Esri
  documentation, with unresolved questions recorded explicitly
* Bounded experiments that preserve proposals, screenshots, limitations, and
  next steps without treating experimental output as authoritative

This is a documentation and architecture library, not a deployable application,
SDK, or automated integration package. Use it to plan and validate your own
implementation; it does not provision Azure or Fabric resources, bundle Esri
Asset Packages, or establish a production-ready architecture for every scenario.

## Start Here

| # | Section | What it covers |
|---|---|---|
| 01 | [Microsoft + Esri Foundation](01-Microsoft-Esri-Foundation/) | The story in one view: what Microsoft Fabric and Esri do together |
| 02 | [ArcGIS GeoAnalytics for Microsoft Fabric](02-GeoAnalytics-for-Fabric/) | Spatial processing in Fabric Spark: guidance, end-to-end scenario, evidence |
| 03 | [ArcGIS Maps for Microsoft Fabric](03-ArcGIS-Maps-for-Fabric/) | Mapping, visualization, exploration, and location-aware experiences in Fabric |
| 04 | [Fabric IQ + Spatial Intelligence](04-Fabric-IQ-Spatial-Intelligence/) | Preview ontology pattern over governed entities and precomputed spatial relationships |
| 05 | [Microsoft + Esri Agentic Reference Pattern](05-Microsoft-Esri-Agentic-Reference-Pattern/) | Conceptual agentic reasoning grounded in Microsoft and Esri context |

See the **[Architecture Map](Architecture-Mapping.md)** for the full library, including near-term and future horizons and how components connect.

## Choose Your Starting Point

The numbered sections organize the library; they are not five mandatory
deployment stages. Start with the foundation for context, then select the
component that matches your customer question.

| Your goal                                      | Start with                                                                                                              |
|------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------|
| Understand the Microsoft + Esri story           | [Microsoft + Esri Foundation](01-Microsoft-Esri-Foundation/README.md)                                                       |
| Plan spatial processing in Fabric              | [GeoAnalytics customer guidance](02-GeoAnalytics-for-Fabric/01-Customer-Guidance.md)                                        |
| Follow a mapping and visualization scenario     | [ArcGIS Maps end-to-end scenario](03-ArcGIS-Maps-for-Fabric/02-End-to-End-Scenario.md)                                       |
| Get from Fabric capacity to an ontology proposal | [Five-step ontology experiment walkthrough](02-GeoAnalytics-for-Fabric/Experiments/Fabric-Ontology/customer-walkthrough.md) |
| Explore Esri domain-model grounding             | [Utility Network-grounded ontology quickstart](04-Fabric-IQ-Spatial-Intelligence/Quickstart-Utility-Network-Ontology.md)     |
| Review readiness and governance                 | [Security and Governance Readiness](01-Microsoft-Esri-Foundation/Security-and-Governance-Readiness.md)                       |
| Explore future agentic possibilities            | [Conceptual agentic reference pattern](05-Microsoft-Esri-Agentic-Reference-Pattern/README.md)                                |

For an implementation discussion, read the selected component's customer guidance
and scenario, review its prerequisites and architecture, then use the evidence
records to distinguish documented behavior from assumptions. Define a small
validation target before investing in a broader deployment.

## Experiments and Maturity Boundaries

The [Fabric Ontology experiment](02-GeoAnalytics-for-Fabric/Experiments/Fabric-Ontology/README.md)
records an initial AI-generated Utility Network conceptual proposal and the setup
journey leading to it. V0 was not generated from an Esri Asset Package or validated
against an authoritative Esri schema. Its next phase is evidence-based grounding
and comparison, not a claim of native ArcGIS Utility Network integration.

The [Fabric IQ spatial-intelligence pattern](04-Fabric-IQ-Spatial-Intelligence/README.md)
provides bounded preview guidance. The
[agentic reference pattern](05-Microsoft-Esri-Agentic-Reference-Pattern/README.md)
remains conceptual. Neither should be read as a supported end-to-end Microsoft +
Esri integration or a committed product roadmap.

Before a customer demo or production decision, confirm current licensing,
capacity, regional availability, tenant settings, source permissions, and support
requirements. A documented product capability does not by itself validate a
customer's complete architecture.

## Source Standard

Documented product claims are linked to authoritative Microsoft and Esri sources
in the component evidence and source registers, where available. Open evidence
gaps, conceptual connections, and experimental hypotheses are identified
separately; they are not established product claims.

Diagrams labeled as scenario views are repository-authored adaptations, not
Microsoft- or Esri-published architectures. This library's synthesis and
experiments do not replace official product documentation or support commitments.
