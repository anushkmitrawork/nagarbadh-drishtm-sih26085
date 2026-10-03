# 🗺️ Geospatial Modelling

## Purpose

The geospatial component establishes the physical and analytical representation of the urban study area.

## Core terrain workflow

```text
DEM
 ↓
Projection / spatial preparation
 ↓
Terrain conditioning
 ↓
Slope / aspect
 ↓
Flow direction
 ↓
Flow accumulation
 ↓
Hydrological indices
 ↓
Streams / watersheds
 ↓
Waterlogging / risk layers
```

## Key outputs

The project includes terrain, hydrological and risk-oriented layers such as:

- DEM and terrain derivatives
- Slope
- Aspect
- Flow direction
- Flow accumulation
- TWI
- TRI
- Watersheds
- Streams
- Drainage density
- Ponding susceptibility
- Waterlogging / risk indicators

The broader current system contains **54 GIS layers** grouped into functional categories.

---

## Spatial framework

The project uses a common projected spatial framework for integration of raster and vector modelling outputs.

The workflow includes an EPSG:32643 / UTM Zone 43N spatial framework for the Pune study area.
