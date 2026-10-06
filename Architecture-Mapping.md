# Architecture Map

This map shows every component in the Microsoft + Esri Architecture Library, where it sits in the Microsoft + Esri landscape, and its current status.

---

## Library Components

| # | Horizon | Component | Role | Folder | Status |
|---|---|---|---|---|---|
| 01 | Foundation | Microsoft + Esri Foundation | Story in one view and landscape introduction | [01-Microsoft-Esri-Foundation](01-Microsoft-Esri-Foundation/) | In progress |
| 02 | Current | ArcGIS GeoAnalytics for Microsoft Fabric | Spatial processing and enrichment in Fabric Spark | [02-GeoAnalytics-for-Fabric](02-GeoAnalytics-for-Fabric/) | In progress |
| 03 | Current | ArcGIS Maps for Microsoft Fabric | Mapping and spatial visualization within Fabric | — | Planned |
| 04 | Current | ArcGIS for Power BI | Location-aware reporting for business users | — | Planned |
| 05 | Current | ArcGIS for Microsoft 365 | Maps and Copilot agent experiences in Teams, SharePoint, and Excel | — | Planned |
| 06 | Current | ArcGIS on Microsoft Azure | Hosting ArcGIS Enterprise on Azure infrastructure | — | Planned |
| — | Near-term | GeoIQ | Reusable location intelligence layer | Reference pattern, once validated | Not started |
| — | Future | ArcGIS MCP Server and location-aware agents | Geospatial reasoning for AI and agents | Reference pattern, once validated | Not started |

Near-term and future items are opportunities under exploration, not committed product roadmap items.

---

## How Components Connect

| From | To | Connection |
|---|---|---|
| 02 GeoAnalytics, [Stage 3](02-GeoAnalytics-for-Fabric/05-Stage-3-Use-the-Results.md) | 03 Maps for Fabric | Spatially enriched output explored on maps in Fabric |
| 02 GeoAnalytics, [Stage 3](02-GeoAnalytics-for-Fabric/05-Stage-3-Use-the-Results.md) | 04 ArcGIS for Power BI | Spatially enriched output used in location-aware reports |

---

## Component Folder Standard

Each component folder follows the same structure:

| File | Purpose |
|---|---|
| `README.md` | Start here: purpose and reading order |
| `01-Customer-Guidance.md` | Where the component fits, proof-of-concept framework, discovery |
| `02-End-to-End-Scenario.md` | Overview of the customer journey |
| `03-...`, `04-...`, `05-...` | One page per stage |
| `Architecture.md` | Component architecture and dependencies |
| `records/Evidence.md` | Claims mapped to authoritative sources, plus open gaps |
| `records/Source-Register.md` | Authoritative sources |
| `images/` | Diagrams |
