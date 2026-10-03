# 🔬 Research Evolution

The project can be understood as a sequence of progressively deeper research questions.

## Question 1 — Where does water go?

**Representation:** Analytical GIS

Terrain and hydrological modelling established the spatial foundation.

<table><tr><td align="center" valign="top"><img src="../assets/images/terrain/dem-utm43n.png" width="310" alt="DEM (UTM 43N), 378 to 729 m"><br><sub>DEM (UTM 43N), 378 to 729 m</sub></td><td align="center" valign="top"><img src="../assets/images/hydrology/flow-accumulation.png" width="310" alt="Flow accumulation"><br><sub>Flow accumulation</sub></td></tr></table>

---

## Question 2 — Why does it accumulate there?

**Representation:** Hydro-spatial risk analysis

Terrain-derived and hydrological indicators were combined to understand waterlogging susceptibility.

<table><tr><td align="center" valign="top"><img src="../assets/images/hydrology/twi.png" width="230" alt="Topographic wetness index"><br><sub>Topographic wetness index</sub></td><td align="center" valign="top"><img src="../assets/images/hydrology/ponding-susceptibility.png" width="230" alt="Ponding susceptibility class"><br><sub>Ponding susceptibility class</sub></td><td align="center" valign="top"><img src="../assets/images/risk/waterlogging-risk.png" width="230" alt="Waterlogging risk index (1 to 5)"><br><sub>Waterlogging risk index (1 to 5)</sub></td></tr></table>

---

## Question 3 — How does the drainage system respond?

**Representation:** Hydraulic modelling

The project introduced an explicit drainage network and SWMM-based simulation.

<table><tr><td align="center" valign="top"><img src="../assets/images/drainage/drainage-design-v2.png" width="310" alt="Drainage design (Fixed v2)"><br><sub>Drainage design (Fixed v2)</sub></td><td align="center" valign="top"><img src="../assets/images/swmm/v7-3hr80-overview.png" width="310" alt="SWMM V7 (3 h): links by max depth / full depth, nodes by status"><br><sub>SWMM V7 (3 h): links by max depth / full depth, nodes by status</sub></td></tr></table>

---

## Question 4 — Where does hydraulic response become surface flooding?

**Representation:** Inundation modelling

Hydraulic outputs were connected to spatial flood-depth products.

<table><tr><td align="center" valign="top"><img src="../assets/images/inundation/flood-depth.png" width="440" alt="Flood depth (m), 0.02 to 1.58 m"><br><sub>Flood depth (m), 0.02 to 1.58 m</sub></td></tr></table>

---

## Question 5 — Which roads become affected?

**Representation:** Decision support

Flood-depth thresholds were translated into road-accessibility information.

<table><tr><td align="center" valign="top"><img src="../assets/images/road-accessibility/impassable-15cm.png" width="230" alt="Impassable at 0.15 m"><br><sub>Impassable at 0.15 m</sub></td><td align="center" valign="top"><img src="../assets/images/road-accessibility/impassable-30cm.png" width="230" alt="Impassable at 0.30 m"><br><sub>Impassable at 0.30 m</sub></td><td align="center" valign="top"><img src="../assets/images/road-accessibility/impassable-50cm.png" width="230" alt="Impassable at 0.50 m"><br><sub>Impassable at 0.50 m</sub></td></tr></table>

---

## Question 6 — How can short-term rainfall information drive the workflow?

**Representation:** Nowcasting-oriented system

SIH 2026 provided the problem context for extending the existing foundation toward an urban flood nowcasting workflow.

<table><tr><td align="center" valign="top"><img src="../assets/images/nowcasting/nowcast-cloudburst-75mm.png" width="440" alt="Nowcast scenario layer: Cloudburst 75mm"><br><sub>Nowcast scenario layer: Cloudburst 75mm</sub></td></tr></table>

<sub>Event/scenario layer; legend units are not labelled in the export.</sub>

---

## The progression

```text
GIS
 ↓
Hydro-spatial modelling
 ↓
Drainage modelling
 ↓
Hydraulics
 ↓
Inundation
 ↓
Road accessibility
 ↓
Nowcasting / decision support
```

This progression is the research evolution of the project, not a claim that every stage belongs to the same manuscript.
