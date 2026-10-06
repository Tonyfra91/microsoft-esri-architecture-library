# ArcGIS GeoAnalytics for Microsoft Fabric Evidence Register

## Purpose

This document records architecture statements and links them to authoritative source material.

---

## Evidence Inventory

| ID | Architecture Claim | Source ID | Source | Status |
|----|--------------------|------------|--------|--------|
| GEO-001 | GeoAnalytics executes through Fabric Spark notebooks and Spark job definitions. | SRC-MSFT-004; SRC-GEO-001 | ArcGIS GeoAnalytics for Microsoft Fabric (Microsoft Learn); ArcGIS GeoAnalytics for Microsoft Fabric | Supported by Microsoft Learn |
| GEO-002 | GeoAnalytics provides spatial SQL functions. | SRC-MSFT-004; SRC-GEO-002 | ArcGIS GeoAnalytics for Microsoft Fabric (Microsoft Learn); ArcGIS GeoAnalytics Documentation | Partial: Microsoft Learn cites 160+ spatial functions but not "spatial SQL"; confirm with Esri source |
| GEO-003 | GeoAnalytics provides track functions. | SRC-MSFT-004; SRC-GEO-002 | ArcGIS GeoAnalytics for Microsoft Fabric (Microsoft Learn); ArcGIS GeoAnalytics Documentation | Partial: Microsoft Learn describes track analysis but not "track functions"; confirm with Esri source |
| GEO-004 | GeoAnalytics provides analysis tools operating on Spark DataFrames. | SRC-MSFT-004; SRC-GEO-003 | ArcGIS GeoAnalytics for Microsoft Fabric (Microsoft Learn); ArcGIS GeoAnalytics Documentation | Supported by Microsoft Learn |
| GEO-005 | GeoAnalytics requires authorization before functions or tools can execute. | SRC-MSFT-004; SRC-GEO-003 | ArcGIS GeoAnalytics for Microsoft Fabric (Microsoft Learn); ArcGIS GeoAnalytics Get Started Guide | Supported by Microsoft Learn |
| GEO-006 | GeoAnalytics operates within Fabric Spark environments. | SRC-MSFT-004; SRC-MSFT-001 | ArcGIS GeoAnalytics for Microsoft Fabric (Microsoft Learn); Apache Spark Runtime in Fabric | Supported by Microsoft Learn (supported runtime versions not stated) |
| ING-001 | Data can be loaded into a lakehouse through file upload, shortcuts, Dataflow Gen2, data pipelines, notebook code, and Eventstream. | SRC-MSFT-005 | Options to Get Data into the Lakehouse | Pending |
| ING-002 | OneLake shortcuts make external data available without copying it. | SRC-MSFT-010 | OneLake Shortcuts | Pending |
| ING-003 | Mirroring replicates data from supported databases and other sources into OneLake. | SRC-MSFT-009 | Mirroring in Microsoft Fabric | Pending |
| ING-004 | GeoAnalytics reads CSV, feature service, file geodatabase, GeoJSON, GeoParquet, ORC, Parquet, and shapefile sources; file geodatabase is read-only. | SRC-GEO-004 | GeoAnalytics Data Sources | Pending |
| ING-005 | GeoAnalytics reads ArcGIS Online and ArcGIS Enterprise feature services into Spark DataFrames; secured services require a registered GIS or a token. | SRC-GEO-005 | GeoAnalytics Feature Service | Pending |
| ING-006 | When writing to Delta, GeoAnalytics converts geometry to WKB; geometry must be converted back when reading Delta tables. | SRC-MSFT-004 | ArcGIS GeoAnalytics for Microsoft Fabric (Microsoft Learn) | Pending |
| ING-007 | A spatial reference should be set on geometry columns that lack one, using the spatial reference in which the data was collected. | SRC-GEO-006 | GeoAnalytics Coordinate Systems | Pending |

---

## Open Evidence Gaps

| ID | Gap | Status |
|----|-----|--------|
| GAP-001 | Published deployment architecture diagram from Microsoft or Esri | Open |
| GAP-002 | Official security architecture documentation specific to GeoAnalytics authorization patterns | Open |

---

## Last Review Date

2026-10-06

## Owner

Tony Franklin
