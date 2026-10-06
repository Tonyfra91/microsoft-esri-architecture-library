# ArcGIS GeoAnalytics for Microsoft Fabric Evidence Register

## Purpose

This document records architecture statements and links them to authoritative source material.

---

## Evidence Inventory

| ID | Architecture Claim | Source ID | Source | Status |
|----|--------------------|------------|--------|--------|
| GEO-001 | GeoAnalytics executes through Fabric Spark notebooks and Spark job definitions. | SRC-MSFT-004; SRC-GEO-001 | ArcGIS GeoAnalytics for Microsoft Fabric (Microsoft Learn); ArcGIS GeoAnalytics for Microsoft Fabric | Supported by Microsoft Learn |
| GEO-002 | GeoAnalytics provides spatial SQL functions. | SRC-GEO-007; SRC-GEO-001; SRC-MSFT-004 | GeoAnalytics SQL Functions; GeoAnalytics Overview; ArcGIS GeoAnalytics for Microsoft Fabric (Microsoft Learn) | Supported: Esri states the `sql` module includes over 150 functions that extend the Spark SQL API for spatial queries |
| GEO-003 | GeoAnalytics provides track functions. | SRC-GEO-008; SRC-GEO-001; SRC-MSFT-004 | GeoAnalytics Track Functions; GeoAnalytics Overview; ArcGIS GeoAnalytics for Microsoft Fabric (Microsoft Learn) | Supported: Esri states the `tracks` module includes functions for managing and analyzing track data |
| GEO-004 | GeoAnalytics provides analysis tools operating on Spark DataFrames. | SRC-GEO-002; SRC-MSFT-004 | GeoAnalytics Tools; ArcGIS GeoAnalytics for Microsoft Fabric (Microsoft Learn) | Supported: Esri states the toolset operates on Spark DataFrames to manage, enrich, summarize, or analyze entire datasets |
| GEO-005 | GeoAnalytics requires authorization before functions or tools can execute. | SRC-MSFT-004; SRC-GEO-003 | ArcGIS GeoAnalytics for Microsoft Fabric (Microsoft Learn); ArcGIS GeoAnalytics Get Started Guide | Supported by Microsoft Learn |
| GEO-006 | GeoAnalytics operates within Fabric Spark environments. | SRC-MSFT-004; SRC-MSFT-001 | ArcGIS GeoAnalytics for Microsoft Fabric (Microsoft Learn); Apache Spark Runtime in Fabric | Supported by Microsoft Learn (supported runtime versions not stated) |
| ING-001 | Data can be loaded into a lakehouse through file upload, shortcuts, Dataflow Gen2, data pipelines, notebook code, and Eventstream. | SRC-MSFT-005 | Options to Get Data into the Lakehouse | Supported: Microsoft lists all six approaches |
| ING-002 | OneLake shortcuts make internal and external data available in OneLake without creating edge copies; optional shortcut caching stores files in a workspace cache. | SRC-MSFT-010 | OneLake Shortcuts | Supported (claim narrowed: original "without copying" did not account for caching) |
| ING-003 | Mirroring continuously replicates data from supported databases and other sources into OneLake. | SRC-MSFT-009 | Mirroring in Microsoft Fabric | Supported (applies to supported sources only) |
| ING-004 | GeoAnalytics reads CSV, feature service, file geodatabase, GeoJSON, GeoParquet, ORC, Parquet, and shapefile sources; file geodatabase is read-only. | SRC-GEO-004 | GeoAnalytics Data Sources | Supported: matches Esri load/save table |
| ING-005 | GeoAnalytics reads ArcGIS Online and ArcGIS Enterprise feature services into Spark DataFrames; secured services require a registered GIS or a token. | SRC-GEO-005 | GeoAnalytics Feature Service | Supported |
| ING-006 | When writing to Delta, GeoAnalytics converts geometry to well-known binary (WKB); when reading those Delta tables, check the column type and convert back to geometry with functions such as ST_GeomFromBinary. | SRC-MSFT-004 | ArcGIS GeoAnalytics for Microsoft Fabric (Microsoft Learn) | Supported (claim reworded to match source: check column type rather than always convert) |
| ING-007 | A spatial reference should be set on geometry columns that lack one, using the spatial reference in which the data was collected. | SRC-GEO-006 | GeoAnalytics Coordinate Systems | Supported |
| SEC-001 | A tenant administrator must enable the ArcGIS GeoAnalytics for Fabric Runtime tenant setting; when disabled, the library is unavailable in Spark notebooks and Spark job definitions. | SRC-MSFT-015; SRC-MSFT-004; SRC-GEO-010 | Tenant Settings Index; Microsoft Learn GeoAnalytics; GeoAnalytics FAQ | Supported |
| SEC-002 | GeoAnalytics is authorized with a username and password, an API key, or a credentials file, each authorizing over the internet using OAuth 2.0; a Spark configuration property (`geoanalytics.auth.cred.file`) can also be set before import. | SRC-GEO-009; SRC-MSFT-004 | GeoAnalytics Authorization; Microsoft Learn GeoAnalytics | Supported |
| SEC-003 | Credentials can be stored in Azure Key Vault and retrieved with `notebookutils.credentials.getSecret`; Esri recommends following customer security/IT policies for credential storage. | SRC-GEO-009 | GeoAnalytics Authorization | Supported |
| SEC-004 | For authentication and usage tracking, GeoAnalytics calls Esri services outside of Fabric and is currently not supported when Outbound Access Protection is enabled. | SRC-MSFT-004 | Microsoft Learn GeoAnalytics | Supported |
| SEC-005 | GeoAnalytics functions and tools run entirely within the user's Fabric environment; processed data is not transmitted outside it unless explicitly requested (for example, writing to an Esri-hosted feature service). | SRC-GEO-010 | GeoAnalytics FAQ | Supported |
| SEC-006 | Anonymized telemetry (usage statistics and function names) may be aggregated and reported, without identifying the Fabric user, workspace, or tenant, and may be stored outside the customer's geographic region. | SRC-GEO-010 | GeoAnalytics FAQ | Supported |

---

## Open Evidence Gaps

| ID | Gap | Status | Validation Notes (2026-10-06) |
|----|-----|--------|-------------------------------|
| GAP-001 | Published deployment architecture diagram from Microsoft or Esri | Open (confirmed) | No GeoAnalytics-specific deployment diagram found on Microsoft Learn (SRC-MSFT-004), Esri Developer docs (SRC-GEO-001, SRC-GEO-009, SRC-GEO-010), or the ArcGIS Architecture Center (SRC-GEO-011). The Architecture Center describes the integration in text only. Scenario views in this repo remain labeled as adapted. |
| GAP-002 | Official security architecture documentation specific to GeoAnalytics authorization patterns | Partially closed | Authorization methods, credential storage, tenant control, outbound calls, and data handling are now documented (SEC-001 to SEC-006). No consolidated security architecture document exists; remaining items tracked in GAP-003. |
| GAP-003 | Network requirements for GeoAnalytics outbound calls: Esri endpoints/hostnames, firewall allow-listing, and behavior with managed virtual networks or Private Link | Open | SRC-MSFT-004 confirms outbound calls to Esri services and lack of support with Outbound Access Protection, but no source lists endpoints or other network requirements. Candidate for an Esri/Microsoft engineering inquiry. |

---

## Last Review Date

2026-10-06

## Owner

Tony Franklin
