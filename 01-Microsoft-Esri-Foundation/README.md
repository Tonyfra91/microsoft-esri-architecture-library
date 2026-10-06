# Microsoft + Esri Foundation

> **Status:** In progress. The five-step diagram (v0.2) and the detailed view (v0.6) are drafts; the integration landscape is current.

## Purpose

This section introduces the Microsoft + Esri story before going into individual components. It answers one question: **what do Microsoft Fabric and Esri do together, and why does it matter to the customer?**

Each component folder that follows (GeoAnalytics, Maps for Fabric, Power BI) goes deeper into one part of that story, with its own customer guidance, end-to-end scenario, and reference architecture.

---

## The Story in One View

![Microsoft + Esri in Five Steps](images/microsoft-esri-five-steps.png)

1. **Data sources to Fabric.** Esri and business data flow into Microsoft Fabric, copied into OneLake or read in place from ArcGIS.
2. **Fabric to Microsoft IQ.** After spatial enrichment with ArcGIS GeoAnalytics, Microsoft IQ models and indexes the data so agents understand what it means. The data stays in OneLake.
3. **Microsoft IQ to agents and apps.** Grounded context powers agents, reports, maps, and conversations, with a person approving before any action.
4. **Agents and apps to people.** Outcomes reach each persona in the tool, and Esri user type, that fits their role.
5. **Back to the source.** Decisions and edits flow back to Esri and business systems.

### The Detailed View

The same story with named components. The numbered bubbles match the steps above, plus step 6: Work IQ exchanges context and answers with Microsoft 365.

![Microsoft + Esri: From Location Data to Location-Aware Agents](images/microsoft-esri-elevator-pitch.png)

The column headings (1 to 5) describe each stage. The blue bubbles mark the flows between them.

| Column | What happens |
|---|---|
| 1 · Data sources | Esri, business, and Microsoft 365 data are where the story starts. |
| 2 · Ingest and enrich | Data is copied into OneLake or read in place from ArcGIS, then enriched spatially with ArcGIS GeoAnalytics running inside Fabric Spark. |
| 3 · Ground | Microsoft IQ (Fabric IQ, Foundry IQ, Work IQ) gives agents and people shared business context. |
| 4 · Act and serve | Agents propose actions, a person approves them, and results reach Power BI, ArcGIS Maps for Fabric, Teams, Activator, and ArcGIS apps. |
| 5 · Personas | Each audience is matched to the Esri user type it typically needs (illustrative). |

The band beneath the diagram is the adoption path: **Crawl** (unify the data), **Walk** (ground it with IQ), **Run** (act with agents and human approval).

**What leaves Fabric.** The dashed Esri licensing service is the only call GeoAnalytics makes on its own: license authorization and usage reporting over HTTPS to arcgis.com. Feature-service reads and writes and basemap tiles happen only when the customer's code asks for them. See [Evidence SEC-007 to SEC-009](../02-GeoAnalytics-for-Fabric/records/Evidence.md).

These views introduce the story. The landscape below shows the wider portfolio and horizons. Implementation detail lives in each component folder.

---

## Microsoft + Esri Fabric Integration Landscape

Organizations increasingly need to combine enterprise business data with location intelligence to improve planning, operations, asset management, customer engagement, and decision-making.

Microsoft Fabric provides the enterprise data and analytics foundation. Esri extends that foundation with geospatial intelligence, enabling organizations to combine business data, operational data, and location data within a shared analytics environment.

The opportunity is not simply to visualize data on a map. The opportunity is to help customers unify enterprise and geospatial data so that location becomes part of analytics, decision-making, and AI workflows. By combining organizational data with spatial relationships, proximity, movement, networks, and geographic context, customers can uncover insights that traditional business intelligence alone cannot provide.

### Current Microsoft + Esri Integration Portfolio

The current Microsoft + Esri Fabric landscape is anchored by three capabilities that are available today:

| Capability | Purpose |
|------------|----------|
| **ArcGIS GeoAnalytics for Microsoft Fabric** | Distributed geospatial analytics running within Fabric Spark environments |
| **ArcGIS Maps for Microsoft Fabric** | Native mapping and spatial visualization within Fabric |
| **ArcGIS for Power BI** | Location-aware dashboards and reporting for business users |

Together, these capabilities enable customers to move from storing and governing data in Microsoft Fabric to performing geospatial analysis, visualizing results geographically, and delivering location-aware insights through existing analytics workflows.

![Microsoft + Esri Fabric Integration Landscape](images/fabric-esri-landscape-v2.png)

## Understanding the Landscape

The diagram is organized around three horizons: current capabilities, near-term validation efforts, and future opportunities.

### Current (Available Today)

The current Microsoft + Esri portfolio focuses on helping customers incorporate geospatial intelligence directly into Fabric and Power BI workflows.

**Current capabilities include:**

- ArcGIS GeoAnalytics for Microsoft Fabric
- ArcGIS Maps for Microsoft Fabric
- ArcGIS for Power BI

These capabilities are available today and represent the foundation of the Microsoft + Esri Fabric integration portfolio.

### Near-Term (Validation & Development)

The near-term focus is understanding customer demand, validating technical patterns, and identifying where Microsoft and Esri can create additional value.

**Current workstreams include:**

- GeoIQ

> **GeoIQ** is this library's working term, not a Microsoft or Esri product name. It describes a reusable location-intelligence layer that brings Esri spatial context into Microsoft IQ (Fabric IQ, Foundry IQ, and Work IQ), so agents and analytics can reason over where things are and how they relate.
- Customer Strategy Validation
- Microsoft + Esri Architectural Reference Pattern
- Expanded Industry Scenarios

The objective is to validate customer adoption patterns, licensing and deployment considerations, and reusable implementation guidance that can accelerate future customer success.

### Future (Roadmap Opportunities)

The future horizon explores how geospatial intelligence may participate in AI-native and agent-based experiences.

**Future areas of exploration include:**

- ArcGIS MCP Server
- Location-Aware Agents
- Microsoft Foundry Integration
- Copilot and Teams Experiences
- Deeper Microsoft + Esri Interoperability

These opportunities build on the current Fabric foundation and should be informed by customer demand, technical validation, and engineering alignment. They should not be interpreted as committed product roadmap items.

### Reading the Diagram

The landscape follows a simple progression:

**Enterprise Data → Geospatial Intelligence → AI-Powered Outcomes**

1. Microsoft Fabric and OneLake provide the enterprise data foundation.
2. ArcGIS GeoAnalytics for Microsoft Fabric, ArcGIS Maps for Microsoft Fabric, and ArcGIS for Power BI add geospatial analytics, visualization, and location-aware business intelligence.
3. GeoIQ represents a near-term opportunity to create a reusable location intelligence layer across analytics and AI experiences.
4. ArcGIS MCP and location-aware agents represent future opportunities to enable AI systems to reason over and act on geospatial relationships.
5. Customer outcomes include unifying business and geospatial data, operating spatial analytics at enterprise scale, delivering location-aware insights, and accelerating decision-making across industries.

> **Executive Takeaway**
>
> Microsoft Fabric provides the enterprise data foundation. Esri contributes geospatial intelligence through analytics, visualization, and business intelligence today, while GeoIQ and future MCP-enabled agent experiences represent opportunities to extend location intelligence into AI-driven workflows.

---

## Components in This Library

| # | Component | Role in the story | Status |
|---|---|---|---|
| 02 | [ArcGIS GeoAnalytics for Microsoft Fabric](../02-GeoAnalytics-for-Fabric/) | Spatial processing and enrichment in Fabric Spark | In progress |
| 03 | ArcGIS Maps for Microsoft Fabric | Mapping and spatial visualization within Fabric | Planned |
| 04 | ArcGIS for Power BI | Location-aware reporting for business users | Planned |

See the [Architecture Map](../Architecture-Mapping.md) for the full library, including near-term and future horizons.

---

## Scope

This section is an introduction, not an implementation guide. Implementation guidance, architectures, and evidence live in each component folder. Near-term and future items (such as GeoIQ, ArcGIS MCP Server, and location-aware agents) are opportunities under exploration, not committed product roadmap items.

---

**Next:** [02 · ArcGIS GeoAnalytics for Microsoft Fabric →](../02-GeoAnalytics-for-Fabric/)
