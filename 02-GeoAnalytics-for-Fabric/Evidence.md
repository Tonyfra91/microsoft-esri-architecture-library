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
