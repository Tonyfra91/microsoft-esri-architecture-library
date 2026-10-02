# ArcGIS GeoAnalytics for Microsoft Fabric Architecture

## Purpose

This document describes the published architecture of ArcGIS GeoAnalytics for Microsoft Fabric based on Microsoft and Esri documentation.

## Architectural Position

ArcGIS GeoAnalytics for Microsoft Fabric is a geospatial analytics capability that executes within Microsoft Fabric Spark environments.

GeoAnalytics is not documented as a standalone compute platform. Published documentation describes GeoAnalytics as operating through Fabric Spark notebooks and Spark job definitions.

## Component Relationship

```text
Microsoft Fabric Platform
        │
        ▼
Fabric Runtime
        │
        ▼
Apache Spark Runtime
        │
        ▼
ArcGIS GeoAnalytics
        │
        ├─ Spatial SQL Functions
        ├─ Track Functions
        └─ Analysis Tools
        │
        ▼
Spatially Enriched Data Products
```

## Dependencies

### Required Platform Components

- Microsoft Fabric
- Fabric Runtime
- Apache Spark
- Lakehouse or supported Fabric data source
- GeoAnalytics authorization

### Related Components

- ArcGIS Maps for Fabric
- ArcGIS for Power BI

## Architecture Questions Answered

1. Where does GeoAnalytics execute?
2. What compute platform does GeoAnalytics use?
3. What capabilities does GeoAnalytics add to Fabric?
4. What downstream analytics experiences can consume outputs?

## Validation Status

Published Product Architecture
