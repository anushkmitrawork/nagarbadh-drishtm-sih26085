# 🗂️ Layer Gallery

Map exports of the project's QGIS layers for the Pune 10 km AOI (circle, r = 10 km, one shared 20.8 km square extent, EPSG:32643).

**Reading notes**

- Colour ramps, classes and stretches (for example p2 to p98) are display styling applied at export. They do not change the underlying data.
- Large continuous layers are stored as 256-colour PNGs (1500 px) to keep the repository light; the QGIS originals are unaffected.
- The nowcast scenario layers are event/scenario products; their legend units are not labelled in the export.
- Layers that were empty at export time (for example SWMM node-depth and link-flow subsets) and intermediate or placeholder layers are not shown.

---

## Overview (QGIS composites)

**Seven-panel pipeline montage**  
<img src="../assets/images/overview/pipeline-montage.png" width="480" alt="Seven-panel pipeline montage">

**DEM over hillshade (55%)**  
<img src="../assets/images/overview/dem-hillshade.png" width="480" alt="DEM over hillshade (55%)">

**Drainage design, retention ponds and outfalls over hillshade**  
<img src="../assets/images/overview/drainage-network.png" width="480" alt="Drainage design, retention ponds and outfalls over hillshade">

**Flood depth with impassable edges at 0.15 / 0.30 / 0.50 m**  
<img src="../assets/images/overview/inundation-road-impact.png" width="480" alt="Flood depth with impassable edges at 0.15 / 0.30 / 0.50 m">

## Terrain

**DEM (UTM 43N), 378 to 729 m**  
<img src="../assets/images/terrain/dem-utm43n.png" width="480" alt="DEM (UTM 43N), 378 to 729 m">

**Hillshade**  
<img src="../assets/images/terrain/hillshade.png" width="480" alt="Hillshade">

**Weighted flow accumulation (signed, p2 to p98 stretch)**  
<img src="../assets/images/terrain/weighted-flow-accumulation.png" width="480" alt="Weighted flow accumulation (signed, p2 to p98 stretch)">

## Hydrological factors

**Slope (degrees)**  
<img src="../assets/images/hydrology/slope.png" width="480" alt="Slope (degrees)">

**Slope risk class**  
<img src="../assets/images/hydrology/slope-risk.png" width="480" alt="Slope risk class">

**Aspect (degrees from north)**  
<img src="../assets/images/hydrology/aspect.png" width="480" alt="Aspect (degrees from north)">

**Terrain ruggedness index (m)**  
<img src="../assets/images/hydrology/tri.png" width="480" alt="Terrain ruggedness index (m)">

**Roughness (m)**  
<img src="../assets/images/hydrology/roughness.png" width="480" alt="Roughness (m)">

**Topographic wetness index**  
<img src="../assets/images/hydrology/twi.png" width="480" alt="Topographic wetness index">

**TWI risk class**  
<img src="../assets/images/hydrology/twi-risk.png" width="480" alt="TWI risk class">

**Depression index (m)**  
<img src="../assets/images/hydrology/depression-index.png" width="480" alt="Depression index (m)">

**Flow direction**  
<img src="../assets/images/hydrology/flow-direction.png" width="480" alt="Flow direction">

**Flow accumulation**  
<img src="../assets/images/hydrology/flow-accumulation.png" width="480" alt="Flow accumulation">

**Flow accumulation risk class**  
<img src="../assets/images/hydrology/flow-accumulation-risk.png" width="480" alt="Flow accumulation risk class">

**Ponding susceptibility class**  
<img src="../assets/images/hydrology/ponding-susceptibility.png" width="480" alt="Ponding susceptibility class">

**Distance to stream (m)**  
<img src="../assets/images/hydrology/stream-proximity.png" width="480" alt="Distance to stream (m)">

**Streams**  
<img src="../assets/images/hydrology/streams.png" width="480" alt="Streams">

**Watersheds**  
<img src="../assets/images/hydrology/watersheds.png" width="480" alt="Watersheds">

**Watershed priority**  
<img src="../assets/images/hydrology/watershed-priority.png" width="480" alt="Watershed priority">

## Risk indices

**Waterlogging risk index (1 to 5)**  
<img src="../assets/images/risk/waterlogging-risk.png" width="480" alt="Waterlogging risk index (1 to 5)">

**Drainage suitability index**  
<img src="../assets/images/risk/drainage-suitability.png" width="480" alt="Drainage suitability index">

**Drainage gap (0 = no gap, 1 = drainage gap)**  
<img src="../assets/images/risk/drainage-gap.png" width="480" alt="Drainage gap (0 = no gap, 1 = drainage gap)">

**High-risk zones**  
<img src="../assets/images/risk/high-risk-zones.png" width="480" alt="High-risk zones">

**Problem / solution class**  
<img src="../assets/images/risk/problem-solution.png" width="480" alt="Problem / solution class">

## Drainage infrastructure

**Drainage design (Fixed v2)**  
<img src="../assets/images/drainage/drainage-design-v2.png" width="480" alt="Drainage design (Fixed v2)">

**Outfall points**  
<img src="../assets/images/drainage/outfall-points.png" width="480" alt="Outfall points">

**Retention ponds**  
<img src="../assets/images/drainage/retention-ponds.png" width="480" alt="Retention ponds">

**Complex intervention zones**  
<img src="../assets/images/drainage/complex-intervention-zones.png" width="480" alt="Complex intervention zones">

**Intervention zones**  
<img src="../assets/images/drainage/intervention-zones.png" width="480" alt="Intervention zones">

**Main flow path**  
<img src="../assets/images/drainage/main-flow-path.png" width="480" alt="Main flow path">

## SWMM results (run V7, 3 h)

**Links by max depth / full depth, nodes by status**  
<img src="../assets/images/swmm/v7-3hr80-overview.png" width="480" alt="Links by max depth / full depth, nodes by status">

**Node status**  
<img src="../assets/images/swmm/v7-3hr80-nodes.png" width="480" alt="Node status">

**Link max depth / full depth**  
<img src="../assets/images/swmm/v7-3hr80-links.png" width="480" alt="Link max depth / full depth">

**200 m window on the flooded nodes**  
<img src="../assets/images/swmm/flooded-nodes-200m-window.png" width="480" alt="200 m window on the flooded nodes">

## Nowcast scenarios and inundation

**Nowcast scenario: Cloudburst 75mm**  
<img src="../assets/images/nowcasting/nowcast-cloudburst-75mm.png" width="480" alt="Nowcast scenario: Cloudburst 75mm">

**Nowcast scenario: 2024-07-25**  
<img src="../assets/images/nowcasting/nowcast-2024-07-25.png" width="480" alt="Nowcast scenario: 2024-07-25">

**Nowcast scenario: 2019-09-25**  
<img src="../assets/images/nowcasting/nowcast-2019-09-25.png" width="480" alt="Nowcast scenario: 2019-09-25">

**Flood depth (m), 0.02 to 1.58 m, cells at or below 0.02 m hidden**  
<img src="../assets/images/inundation/flood-depth.png" width="480" alt="Flood depth (m), 0.02 to 1.58 m, cells at or below 0.02 m hidden">

## Road accessibility

**Impassable edges at 0.15 m**  
<img src="../assets/images/road-accessibility/impassable-15cm.png" width="480" alt="Impassable edges at 0.15 m">

**Impassable edges at 0.30 m**  
<img src="../assets/images/road-accessibility/impassable-30cm.png" width="480" alt="Impassable edges at 0.30 m">

**Impassable edges at 0.50 m**  
<img src="../assets/images/road-accessibility/impassable-50cm.png" width="480" alt="Impassable edges at 0.50 m">
