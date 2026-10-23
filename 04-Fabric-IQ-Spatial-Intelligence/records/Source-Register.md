---
description: Authoritative sources for Fabric IQ patterns and Esri domain-model research.
---

# Fabric IQ + Spatial Intelligence Source Register

## Purpose

This register tracks authoritative sources for the Fabric IQ spatial-intelligence pattern and separates current Microsoft product documentation from unresolved Esri integration research.

## Source Inventory

| Source ID | Source | Publisher | Category | URL | Status |
|---|---|---|---|---|---|
| <a id="src-iq-msft-001"></a>SRC-IQ-MSFT-001 | Microsoft IQ | Microsoft | Product Architecture | https://learn.microsoft.com/en-us/microsoft-iq | Active |
| <a id="src-iq-msft-002"></a>SRC-IQ-MSFT-002 | What is Fabric IQ? | Microsoft | Product Architecture | https://learn.microsoft.com/en-us/fabric/iq/overview | Active |
| <a id="src-iq-msft-003"></a>SRC-IQ-MSFT-003 | Get Started with Fabric IQ | Microsoft | Implementation Guidance | https://learn.microsoft.com/en-us/fabric/iq/get-started-with-fabric-iq | Active |
| <a id="src-iq-msft-004"></a>SRC-IQ-MSFT-004 | What Is Ontology (Preview)? | Microsoft | Product Documentation | https://learn.microsoft.com/en-us/fabric/iq/ontology/overview | Active; preview |
| <a id="src-iq-msft-005"></a>SRC-IQ-MSFT-005 | Ontology (Preview) Required Tenant Settings | Microsoft | Administration Guidance | https://learn.microsoft.com/en-us/fabric/iq/ontology/overview-tenant-settings | Active; preview |
| <a id="src-iq-msft-006"></a>SRC-IQ-MSFT-006 | Ontology Tutorial | Microsoft | Implementation Guidance | https://learn.microsoft.com/en-us/fabric/iq/ontology/tutorial-0-introduction | Active; preview |
| <a id="src-iq-msft-007"></a>SRC-IQ-MSFT-007 | Use the Ontology Agent (Preview) | Microsoft | Product Documentation | https://learn.microsoft.com/en-us/fabric/iq/ontology/how-to-use-ontology-agent | Active; preview |
| <a id="src-iq-msft-008"></a>SRC-IQ-MSFT-008 | Materialize an Ontology Graph (Preview) | Microsoft | Product Documentation | https://learn.microsoft.com/en-us/fabric/iq/ontology/how-to-use-ontology-graph | Active; preview |
| <a id="src-iq-msft-009"></a>SRC-IQ-MSFT-009 | What is Graph in Microsoft Fabric? | Microsoft | Product Documentation | https://learn.microsoft.com/en-us/fabric/graph/overview | Active |
| <a id="src-iq-msft-010"></a>SRC-IQ-MSFT-010 | Power BI Semantic Models in Microsoft Fabric | Microsoft | Product Documentation | https://learn.microsoft.com/en-us/fabric/data-warehouse/semantic-models | Active |
| <a id="src-iq-msft-011"></a>SRC-IQ-MSFT-011 | Fabric Data Agent Creation | Microsoft | Product Documentation | https://learn.microsoft.com/en-us/fabric/data-science/concept-data-agent | Active |
| <a id="src-iq-msft-012"></a>SRC-IQ-MSFT-012 | Consume Fabric Data Agent from Microsoft Foundry via Fabric IQ | Microsoft | Integration Guidance | https://learn.microsoft.com/en-us/fabric/data-science/data-agent-foundry-fabric-iq | Active; preview |
| <a id="src-iq-esri-001"></a>SRC-IQ-ESRI-001 | Utility Network information model | Esri | Domain Model | SOURCE REQUIRED | Open |
| <a id="src-iq-esri-002"></a>SRC-IQ-ESRI-002 | Utility Network Package Asset Package Reference | Esri | Technical Schema and Package Reference | https://doc.arcgis.com/en/arcgis-solutions/latest/tool-reference/utility-network-package/pdf/Utility%20Network%20Package_Asset%20Package%20Reference.pdf | Active |
| <a id="src-iq-esri-003"></a>SRC-IQ-ESRI-003 | ArcGIS Knowledge Graph model information | Esri | Technical Documentation | SOURCE REQUIRED | Open |
| <a id="src-iq-esri-004"></a>SRC-IQ-ESRI-004 | Esri formal ontology availability | Esri | Engineering Confirmation | SOURCE REQUIRED | Open |
| <a id="src-iq-esri-005"></a>SRC-IQ-ESRI-005 | Asset Package machine-readable format and schema coverage | Esri | Technical Schema and Package Reference | https://doc.arcgis.com/en/arcgis-solutions/latest/tool-reference/utility-network-package/pdf/Utility%20Network%20Package_Asset%20Package%20Reference.pdf | Active; bounded to Asset Package |
| <a id="src-iq-esri-006"></a>SRC-IQ-ESRI-006 | Apply Asset Package | Esri | Implementation Guidance | https://doc.arcgis.com/en/arcgis-solutions/latest/tool-reference/utility-network-package/apply-asset-package.htm | Active |
| <a id="src-iq-msft-013"></a>SRC-IQ-MSFT-013 | Ontology Tutorial Part 1: Create an Ontology | Microsoft | Implementation Guidance | https://learn.microsoft.com/en-us/fabric/iq/ontology/tutorial-1-create-ontology | Active; preview; checked 2026-10-23 |
| <a id="src-iq-esri-007"></a>SRC-IQ-ESRI-007 | Introduction to Water Utility Network Foundation | Esri | Package Availability and Requirements | https://doc.arcgis.com/en/arcgis-solutions/latest/reference/introduction-to-water-distribution-utility-network-foundation.htm | Active; Essentials contents and data-dictionary link checked 2026-10-23; dictionary requires JavaScript and package fields remain to be inspected |
| <a id="src-iq-esri-008"></a>SRC-IQ-ESRI-008 | Export Table | Esri | Implementation Guidance | https://doc.esri.com/en/arcgis-pro/latest/tool-reference/conversion/export-table.html | Active; CSV output and description-transfer guidance checked 2026-10-23 |
| <a id="src-iq-esri-009"></a>SRC-IQ-ESRI-009 | Transfer Field Domain Descriptions | Esri | Implementation Guidance | https://doc.esri.com/en/arcgis-pro/latest/tool-reference/environment-settings/transfer-domain-descriptions.html | Active; code and description field behavior checked 2026-10-23 |

## Source Validation Rules

The preferred order of authority is:

1. Microsoft Learn product and administration documentation
2. Esri product and technical documentation
3. Jointly validated Microsoft and Esri content
4. Direct engineering confirmation recorded with date and owner

Preview documentation supports a bounded proof of concept, not an assumption of production support or a committed general-availability design.

## Last Review Date

2026-10-23 (quickstart sources added; existing unresolved sources remain open)

## Component Owner

Architecture team
