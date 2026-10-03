# 🧭 Methodology

## Overview

NagarBadh Drishtm combines geospatial analysis, hydrological modelling, drainage representation, hydraulic simulation and decision-support layers.

The high-level computational pipeline is:

```text
Input spatial data
      ↓
Terrain modelling
      ↓
Hydrological analysis
      ↓
Drainage representation
      ↓
SWMM hydraulic simulation
      ↓
Flood-depth / inundation products
      ↓
Road-accessibility thresholds
      ↓
PostGIS + Dashboard
```

---

## 1. Spatial inputs

The project uses spatial data to establish the urban modelling environment, including terrain and other GIS layers.

The system uses a predominantly indigenous spatial-data foundation, including an ISRO-derived DEM in the project workflow.

---

## 2. Terrain modelling

The terrain stage derives spatial characteristics such as:

- Elevation
- Slope
- Flow direction
- Flow accumulation
- Terrain/hydrological indices
- Watersheds
- Streams and drainage-related features

---

## 3. Hydrological / risk modelling

Terrain and hydrological outputs are translated into spatial indicators related to water movement, ponding susceptibility, waterlogging and flood risk.

The resulting layers become inputs to downstream analysis and decision-support products.

---

## 4. Drainage representation

The drainage stage represents the urban drainage system as a computational network.

The current project documentation includes:

- Drainage conduits
- Nodes
- Outfalls
- Retention ponds
- Intervention-related spatial layers

The model contains **28,370 drainage conduit segments**.

---

## 5. Hydraulic simulation

The drainage network is simulated using **EPA SWMM 5.2.4**, with PySWMM used in the computational workflow.

Relevant outputs include:

- Node depth
- Link flow
- Surcharge/flooding behaviour

The engineering workflow includes iterative diagnosis and correction of numerical instability rather than treating simulation output as automatically valid.

---

## 6. Inundation representation

Hydraulic outputs are connected back to the GIS environment to create spatial flood-depth and inundation-oriented products.

---

## 7. Road accessibility

Flood depth is translated into road-impact layers using:

- 0.15 m
- 0.30 m
- 0.50 m

thresholds.

This turns raw depth into an operationally understandable road-accessibility representation.

---

## 8. Data infrastructure

The system uses:

- PostgreSQL
- PostGIS
- QGIS / PyQGIS

for structured spatial data management and integration of modelling outputs.

---

## 9. Dashboard

The outputs are exposed through the repository's interactive web dashboard.

See [Dashboard Documentation](dashboard.md).

---

## Scope note

The methodology describes the broader current system.

The associated manuscript documents only the research scope represented in that manuscript and should not be treated as a complete record of all later SWMM, inundation, road-accessibility and nowcasting development.
