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

<table><tr><td align="center" valign="top"><img src="../assets/images/terrain/dem-utm43n.png" width="230" alt="DEM (UTM 43N), 378 to 729 m"><br><sub>DEM (UTM 43N), 378 to 729 m</sub></td><td align="center" valign="top"><img src="../assets/images/hydrology/twi.png" width="230" alt="Topographic wetness index"><br><sub>Topographic wetness index</sub></td><td align="center" valign="top"><img src="../assets/images/risk/waterlogging-risk.png" width="230" alt="Waterlogging risk index (1 to 5)"><br><sub>Waterlogging risk index (1 to 5)</sub></td></tr></table>

### 2. Hydraulic layer

The drainage network is represented computationally and simulated with EPA SWMM.

<table><tr><td align="center" valign="top"><img src="../assets/images/drainage/drainage-design-v2.png" width="310" alt="Drainage design (Fixed v2)"><br><sub>Drainage design (Fixed v2)</sub></td><td align="center" valign="top"><img src="../assets/images/swmm/v7-3hr80-overview.png" width="310" alt="SWMM V7 (3 h): links by max depth / full depth, nodes by status"><br><sub>SWMM V7 (3 h): links by max depth / full depth, nodes by status</sub></td></tr></table>

### 3. Flood-impact layer

Hydraulic outputs are translated into inundation/flood-depth products and road-accessibility thresholds.

<table><tr><td align="center" valign="top"><img src="../assets/images/inundation/flood-depth.png" width="310" alt="Flood depth (m), 0.02 to 1.58 m"><br><sub>Flood depth (m), 0.02 to 1.58 m</sub></td><td align="center" valign="top"><img src="../assets/images/road-accessibility/impassable-30cm.png" width="310" alt="Impassable at 0.30 m"><br><sub>Impassable at 0.30 m</sub></td></tr></table>

### 4. Data layer

PostgreSQL/PostGIS provides structured spatial data management.

### 5. Presentation layer

The interactive dashboard exposes project outputs to users.

---

## Engineering principle

The system follows a practical loop:

**Build → Simulate → Debug → Verify → Present**

The architecture therefore reflects not only the final data flow, but also the iterative nature of computational modelling.
