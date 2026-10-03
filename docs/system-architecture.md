# 🏗️ System Architecture

## High-level architecture

```text
                 DATA SOURCES
                      │
       ┌──────────────┼──────────────┐
       ↓              ↓              ↓
      DEM        Spatial Data    Event/Scenario
       │              │              │
       └──────────────┼──────────────┘
                      ↓
             GEOSPATIAL PROCESSING
                      ↓
             HYDROLOGICAL MODEL
                      ↓
             DRAINAGE NETWORK
                      ↓
               EPA SWMM 5.2.4
                      ↓
             HYDRAULIC OUTPUTS
                      ↓
             INUNDATION PRODUCTS
                      ↓
             ROAD ACCESSIBILITY
                      ↓
             PostgreSQL / PostGIS
                      ↓
                 DASHBOARD
```

---

## System layers

### 1. Spatial layer

The GIS environment provides the terrain, hydrological factors, risk layers and infrastructure representation.

### 2. Hydraulic layer

The drainage network is represented computationally and simulated with EPA SWMM.

### 3. Flood-impact layer

Hydraulic outputs are translated into inundation/flood-depth products and road-accessibility thresholds.

### 4. Data layer

PostgreSQL/PostGIS provides structured spatial data management.

### 5. Presentation layer

The interactive dashboard exposes project outputs to users.

---

## Engineering principle

The system follows a practical loop:

**Build → Simulate → Debug → Verify → Present**

The architecture therefore reflects not only the final data flow, but also the iterative nature of computational modelling.
