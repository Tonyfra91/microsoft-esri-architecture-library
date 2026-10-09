# Architecture Map

This map shows every component in the Microsoft + Esri Architecture Library, where it sits in the Microsoft + Esri landscape, and its current status.

---

## Library Components

| # | Horizon | Component | Role | Folder | Status |
|---|---|---|---|---|---|
| 01 | Foundation | Microsoft + Esri Foundation | Story in one view and landscape introduction | [01-Microsoft-Esri-Foundation](01-Microsoft-Esri-Foundation/) | In progress |
| 02 | Current | ArcGIS GeoAnalytics for Microsoft Fabric | Spatial processing and enrichment in Fabric Spark | [02-GeoAnalytics-for-Fabric](02-GeoAnalytics-for-Fabric/) | In progress |
| 03 | Current | ArcGIS Maps for Microsoft Fabric | Mapping, visualization, exploration, and location-aware experiences in Fabric | [03-ArcGIS-Maps-for-Fabric](03-ArcGIS-Maps-for-Fabric/) | Validation framework |
| 04 | Exploration | Fabric IQ + Spatial Intelligence | Business context, ontology, semantic models, graph, data agents, and spatial grounding | [04-Fabric-IQ-Spatial-Intelligence](04-Fabric-IQ-Spatial-Intelligence/) | Validation required |
| 05 | Conceptual | Microsoft + Esri Agentic Reference Pattern | Foundry, Fabric IQ, agents, ArcGIS MCP, tools, and Ground Truth | [05-Microsoft-Esri-Agentic-Reference-Pattern](05-Microsoft-Esri-Agentic-Reference-Pattern/) | Conceptual pattern |

Exploration and conceptual items are validation areas, not supported product integrations or committed product roadmap items.

---

## How Components Connect

| From | To | Connection |
|---|---|---|
| 02 GeoAnalytics, [Stage 3](02-GeoAnalytics-for-Fabric/05-Stage-3-Use-the-Results.md) | 03 Maps for Fabric | Spatially enriched output explored on maps in Fabric |
| 03 Maps for Fabric | 04 Fabric IQ + Spatial Intelligence | Spatial experiences motivate business, domain, and spatial-context validation |
| 04 Fabric IQ + Spatial Intelligence | 05 Agentic Reference Pattern | Validated context may ground future agent reasoning |

---

## Component Folder Standard

Each component folder follows the same structure:

| File | Purpose |
|---|---|
| `README.md` | Start here: purpose, scope, status, and reading order |
| `01-Customer-Guidance.md` | Customer framing, proof-of-concept framework, and discovery when applicable |
| `Architecture.md` | Component architecture, exploration boundary, or conceptual pattern |
| `Architecture-Mapping.md` | Architecture work products, relationships, and evidence gates |
| `records/Evidence.md` | Claims mapped to authoritative sources, plus open gaps |
| `records/Source-Register.md` | Authoritative sources and collection status |
| `records/Collection-Checklist.md` | Artifacts still required; checklist items are not evidence claims |
| `images/` | Validated or explicitly labeled conceptual diagrams |

Validated components may add end-to-end scenarios and stage pages. Exploration areas add discovery records instead of implying a complete implementation.
