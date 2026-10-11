# ArcGIS GeoAnalytics for Microsoft Fabric Evidence Register

## Purpose

This document records architecture statements and links them to authoritative source material.

---

## Evidence Inventory

| ID | Architecture Claim | Source ID | Source | Status |
|----|--------------------|------------|--------|--------|
| <a id="geo-001"></a>GEO-001 | GeoAnalytics executes through Fabric Spark notebooks and Spark job definitions. | [SRC-MSFT-004](Source-Register.md#src-msft-004); [SRC-GEO-001](Source-Register.md#src-geo-001) | ArcGIS GeoAnalytics for Microsoft Fabric (Microsoft Learn); ArcGIS GeoAnalytics for Microsoft Fabric | Supported by Microsoft Learn |
| <a id="geo-002"></a>GEO-002 | GeoAnalytics provides spatial SQL functions. | [SRC-GEO-007](Source-Register.md#src-geo-007); [SRC-GEO-001](Source-Register.md#src-geo-001); [SRC-MSFT-004](Source-Register.md#src-msft-004) | GeoAnalytics SQL Functions; GeoAnalytics Overview; ArcGIS GeoAnalytics for Microsoft Fabric (Microsoft Learn) | Supported: Esri states the `sql` module includes over 150 functions that extend the Spark SQL API for spatial queries |
| <a id="geo-003"></a>GEO-003 | GeoAnalytics provides track functions. | [SRC-GEO-008](Source-Register.md#src-geo-008); [SRC-GEO-001](Source-Register.md#src-geo-001); [SRC-MSFT-004](Source-Register.md#src-msft-004) | GeoAnalytics Track Functions; GeoAnalytics Overview; ArcGIS GeoAnalytics for Microsoft Fabric (Microsoft Learn) | Supported: Esri states the `tracks` module includes functions for managing and analyzing track data |
| <a id="geo-004"></a>GEO-004 | GeoAnalytics provides analysis tools operating on Spark DataFrames. | [SRC-GEO-002](Source-Register.md#src-geo-002); [SRC-MSFT-004](Source-Register.md#src-msft-004) | GeoAnalytics Tools; ArcGIS GeoAnalytics for Microsoft Fabric (Microsoft Learn) | Supported: Esri states the toolset operates on Spark DataFrames to manage, enrich, summarize, or analyze entire datasets |
| <a id="geo-005"></a>GEO-005 | GeoAnalytics requires authorization before functions or tools can execute. | [SRC-MSFT-004](Source-Register.md#src-msft-004); [SRC-GEO-003](Source-Register.md#src-geo-003) | ArcGIS GeoAnalytics for Microsoft Fabric (Microsoft Learn); ArcGIS GeoAnalytics Get Started Guide | Supported by Microsoft Learn |
| <a id="geo-006"></a>GEO-006 | GeoAnalytics operates within Fabric Spark environments. | [SRC-MSFT-004](Source-Register.md#src-msft-004); [SRC-MSFT-001](Source-Register.md#src-msft-001) | ArcGIS GeoAnalytics for Microsoft Fabric (Microsoft Learn); Apache Spark Runtime in Fabric | Supported by Microsoft Learn (supported runtime versions not stated) |
| <a id="ing-001"></a>ING-001 | Data can be loaded into a lakehouse through file upload, shortcuts, Dataflow Gen2, data pipelines, notebook code, and Eventstream. | [SRC-MSFT-005](Source-Register.md#src-msft-005) | Options to Get Data into the Lakehouse | Supported: Microsoft lists all six approaches |
| <a id="ing-002"></a>ING-002 | OneLake shortcuts make internal and external data available in OneLake without creating edge copies; optional shortcut caching stores files in a workspace cache. | [SRC-MSFT-010](Source-Register.md#src-msft-010) | OneLake Shortcuts | Supported (claim narrowed: original "without copying" did not account for caching) |
| <a id="ing-003"></a>ING-003 | Mirroring continuously replicates data from supported databases and other sources into OneLake. | [SRC-MSFT-009](Source-Register.md#src-msft-009) | Mirroring in Microsoft Fabric | Supported (applies to supported sources only) |
| <a id="ing-004"></a>ING-004 | GeoAnalytics reads CSV, feature service, file geodatabase, GeoJSON, GeoParquet, ORC, Parquet, and shapefile sources; file geodatabase is read-only. | [SRC-GEO-004](Source-Register.md#src-geo-004) | GeoAnalytics Data Sources | Supported: matches Esri load/save table |
| <a id="ing-005"></a>ING-005 | GeoAnalytics reads ArcGIS Online and ArcGIS Enterprise feature services into Spark DataFrames; secured services require a registered GIS or a token. | [SRC-GEO-005](Source-Register.md#src-geo-005) | GeoAnalytics Feature Service | Supported |
| <a id="ing-006"></a>ING-006 | When writing to Delta, GeoAnalytics converts geometry to well-known binary (WKB); when reading those Delta tables, check the column type and convert back to geometry with functions such as ST_GeomFromBinary. | [SRC-MSFT-004](Source-Register.md#src-msft-004) | ArcGIS GeoAnalytics for Microsoft Fabric (Microsoft Learn) | Supported (claim reworded to match source: check column type rather than always convert) |
| <a id="ing-007"></a>ING-007 | A spatial reference should be set on geometry columns that lack one, using the spatial reference in which the data was collected. | [SRC-GEO-006](Source-Register.md#src-geo-006) | GeoAnalytics Coordinate Systems | Supported |
| <a id="sec-001"></a>SEC-001 | A tenant administrator must enable the ArcGIS GeoAnalytics for Fabric Runtime tenant setting; when disabled, the library is unavailable in Spark notebooks and Spark job definitions. | [SRC-MSFT-015](Source-Register.md#src-msft-015); [SRC-MSFT-004](Source-Register.md#src-msft-004); [SRC-GEO-010](Source-Register.md#src-geo-010) | Tenant Settings Index; Microsoft Learn GeoAnalytics; GeoAnalytics FAQ | Supported |
| <a id="sec-002"></a>SEC-002 | GeoAnalytics is authorized with a username and password, an API key, or a credentials file, each authorizing over the internet using OAuth 2.0; a Spark configuration property (`geoanalytics.auth.cred.file`) can also be set before import. | [SRC-GEO-009](Source-Register.md#src-geo-009); [SRC-MSFT-004](Source-Register.md#src-msft-004) | GeoAnalytics Authorization; Microsoft Learn GeoAnalytics | Supported |
| <a id="sec-003"></a>SEC-003 | Credentials can be stored in Azure Key Vault and retrieved with `notebookutils.credentials.getSecret`; Esri recommends following customer security/IT policies for credential storage. | [SRC-GEO-009](Source-Register.md#src-geo-009) | GeoAnalytics Authorization | Supported |
| <a id="sec-004"></a>SEC-004 | For authentication and usage tracking, GeoAnalytics calls Esri services outside of Fabric and is currently not supported when Outbound Access Protection is enabled. | [SRC-MSFT-004](Source-Register.md#src-msft-004) | Microsoft Learn GeoAnalytics | Supported |
| <a id="sec-005"></a>SEC-005 | GeoAnalytics functions and tools run entirely within the user's Fabric environment; processed data is not transmitted outside it unless explicitly requested (for example, writing to an Esri-hosted feature service). | [SRC-GEO-010](Source-Register.md#src-geo-010) | GeoAnalytics FAQ | Supported |
| <a id="sec-006"></a>SEC-006 | Anonymized telemetry (usage statistics and function names) may be aggregated and reported, without identifying the Fabric user, workspace, or tenant, and may be stored outside the customer's geographic region. | [SRC-GEO-010](Source-Register.md#src-geo-010) | GeoAnalytics FAQ | Supported |
| <a id="sec-007"></a>SEC-007 | GeoAnalytics outbound calls go over HTTPS on port 443 to the arcgis.com domain, under `/sharing/rest`: OAuth authorization (`/sharing/rest/oauth2`) and periodic usage reporting (`/sharing/rest/portals/self/usage`). | [SRC-GEO-012](Source-Register.md#src-geo-012) | Esri direct confirmation | Supported (Esri direct confirmation, 2026-10-06) |
| <a id="sec-008"></a>SEC-008 | `st.plot()` retrieves basemap tiles from Esri when a basemap is requested (for example `basemap="light"`); this is an outbound call triggered by the user's code. | [SRC-GEO-012](Source-Register.md#src-geo-012); [SRC-GEO-013](Source-Register.md#src-geo-013) | Esri direct confirmation; Visualize results with st.plot() | Supported |
| <a id="sec-009"></a>SEC-009 | Analysis functions and tools make no implicit calls to other ArcGIS services; outbound calls are limited to authorization, usage reporting, user-requested feature-service reads and writes, and basemap tiles for plotting. | [SRC-GEO-012](Source-Register.md#src-geo-012); [SRC-GEO-010](Source-Register.md#src-geo-010) | Esri direct confirmation; GeoAnalytics FAQ | Supported (Esri direct confirmation, 2026-10-06) |
| <a id="out-001"></a>OUT-001 | A spatially enriched Spark DataFrame can be persisted to supported Fabric data items, including Delta tables in a lakehouse. | [SRC-MSFT-004](Source-Register.md#src-msft-004); [SRC-GEO-004](Source-Register.md#src-geo-004) | ArcGIS GeoAnalytics for Microsoft Fabric (Microsoft Learn); GeoAnalytics Data Sources | Supported |
| <a id="out-002"></a>OUT-002 | Fabric output exposed through a Power BI semantic model or report can be visualized with ArcGIS for Power BI. | [SRC-MSFT-018](Source-Register.md#src-msft-018); [SRC-GEO-017](Source-Register.md#src-geo-017); [SRC-GEO-018](Source-Register.md#src-geo-018) | Create ArcGIS Maps for Power BI; Introduction to ArcGIS for Power BI; Configure ArcGIS for Power BI | Supported |
| <a id="out-003"></a>OUT-003 | ArcGIS Maps for Microsoft Fabric can visualize supported Fabric and OneLake data through its documented data-loading workflow. | [SRC-GEO-015](Source-Register.md#src-geo-015); [SRC-GEO-016](Source-Register.md#src-geo-016); [SRC-MSFT-017](Source-Register.md#src-msft-017) | ArcGIS for Microsoft Fabric; ArcGIS Maps for Microsoft Fabric Quick Start Guide; Microsoft Fabric release notes | Supported |
| <a id="out-004"></a>OUT-004 | GeoAnalytics can explicitly write supported Spark DataFrame results to an ArcGIS Online or ArcGIS Enterprise feature service; authorization, service capabilities, and permissions apply. | [SRC-GEO-004](Source-Register.md#src-geo-004); [SRC-GEO-005](Source-Register.md#src-geo-005) | GeoAnalytics Data Sources; GeoAnalytics Feature Service | Supported |

---

## Open Evidence Gaps

| ID | Gap | Status | Validation Notes (2026-10-06) |
|----|-----|--------|-------------------------------|
| <a id="gap-001"></a>GAP-001 | Published deployment architecture diagram from Microsoft or Esri | Open (confirmed) | No GeoAnalytics-specific deployment diagram found on Microsoft Learn ([SRC-MSFT-004](Source-Register.md#src-msft-004)), Esri Developer docs ([SRC-GEO-001](Source-Register.md#src-geo-001), [SRC-GEO-009](Source-Register.md#src-geo-009), [SRC-GEO-010](Source-Register.md#src-geo-010)), or the ArcGIS Architecture Center ([SRC-GEO-011](Source-Register.md#src-geo-011)). The Architecture Center describes the integration in text only. Scenario views in this repo remain labeled as adapted. |
| <a id="gap-002"></a>GAP-002 | Official security architecture documentation specific to GeoAnalytics authorization patterns | Partially closed | Authorization methods, credential storage, tenant control, outbound calls, and data handling are now documented ([SEC-001](#sec-001) to [SEC-006](#sec-006)). No consolidated security architecture document exists. Outbound calls and endpoints confirmed by Esri ([SEC-007](#sec-007) to [SEC-009](#sec-009)); remaining items tracked in [GAP-003](#gap-003). |
| <a id="gap-003"></a>GAP-003 | Network requirements for GeoAnalytics outbound calls: Esri endpoints/hostnames, firewall allow-listing, and behavior with managed virtual networks or Private Link | Partially closed | Closed: Esri confirmed outbound calls use HTTPS on port 443 to arcgis.com under `/sharing/rest` ([SEC-007](#sec-007) to [SEC-009](#sec-009)); allow-listing guidance is sufficient for deployment. Esri did not provide a complete endpoint list because several endpoints are called. Still open: behavior with managed virtual networks or Private Link. |

---

## Last Review Date

2026-10-07

## Owner

Tony Franklin
