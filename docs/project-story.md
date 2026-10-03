# 📖 Project Story

## NagarBadh Drishtm: a research journey

NagarBadh Drishtm is best understood as an evolving research and engineering project.

It did not begin with SIH 2026.

It began as a **second-semester MCA project** focused on understanding urban terrain, hydrology and waterlogging through geospatial analysis.

The project then kept generating better questions. Each question forced the system one layer deeper.

---

## Chapter 1 — Where does water go?

The first stage focused on terrain and hydrological behaviour.

The working idea was straightforward:

**if we understand the shape of the terrain, we can begin to understand how water is likely to move and accumulate.**

This stage established the hydro-spatial foundation of the project.

The core representation was:

```text
DEM
 ↓
Terrain derivatives
 ↓
Hydrological factors
 ↓
Water movement
 ↓
Waterlogging / spatial risk
```

The initial research therefore lived primarily in the GIS domain.

<table><tr><td align="center" valign="top"><img src="../assets/images/terrain/dem-utm43n.png" width="310" alt="DEM (UTM 43N), 378 to 729 m"><br><sub>DEM (UTM 43N), 378 to 729 m</sub></td><td align="center" valign="top"><img src="../assets/images/hydrology/flow-accumulation.png" width="310" alt="Flow accumulation"><br><sub>Flow accumulation</sub></td></tr></table>

---

## Chapter 2 — From GIS layers to a hydro-spatial model

As the project developed, the focus moved beyond simply visualising terrain.

The work began combining terrain-derived hydrological indicators, drainage-related spatial information and risk-oriented layers into a more structured model of urban waterlogging.

The question changed from:

> **Where is low ground?**

to:

> **What combination of terrain and hydrological conditions makes an area vulnerable to waterlogging?**

This became the foundation for the associated manuscript.

<table><tr><td align="center" valign="top"><img src="../assets/images/hydrology/twi.png" width="230" alt="Topographic wetness index"><br><sub>Topographic wetness index</sub></td><td align="center" valign="top"><img src="../assets/images/hydrology/ponding-susceptibility.png" width="230" alt="Ponding susceptibility class"><br><sub>Ponding susceptibility class</sub></td><td align="center" valign="top"><img src="../assets/images/risk/waterlogging-risk.png" width="230" alt="Waterlogging risk index (1 to 5)"><br><sub>Waterlogging risk index (1 to 5)</sub></td></tr></table>

### Important scope distinction

The manuscript represents this **earlier hydro-spatial stage** of the work. It does **not** represent the complete current NagarBadh Drishtm implementation.

---

## Chapter 3 — Research expansion through CIIAR

The work subsequently expanded through the CIIAR program at DES Pune University.

The project moved into broader hydro-spatial research and computational modelling.

This period also opened a new representation of the same geographical problem: **3D computational modelling**.

The GIS environment was prepared as a geographically accurate 3D representation for collaboration with a Unity-based development team.

The project documentation records the user's role as preparation and delivery of the geographically accurate 3D basemap/environment, while the interactive simulation logic was developed by the collaborating game-development team.

---

## Chapter 4 — Why terrain alone was not enough

A terrain model can tell us a great deal about water movement.

But an urban drainage system adds another physical system to the problem.

That led to a new question:

> **What happens when rainfall-driven water interacts with the drainage network?**

The project therefore moved from hydro-spatial analysis into explicit drainage and hydraulic modelling.

This introduced:

- Drainage network representation
- Nodes and conduits
- Outfalls
- Hydraulic simulation
- SWMM outputs
- Hydraulic stress and flooding response

The project now had a second physical representation:

**the drainage system itself.**

<table><tr><td align="center" valign="top"><img src="../assets/images/drainage/drainage-design-v2.png" width="230" alt="Drainage design (Fixed v2)"><br><sub>Drainage design (Fixed v2)</sub></td><td align="center" valign="top"><img src="../assets/images/drainage/outfall-points.png" width="230" alt="Outfall points"><br><sub>Outfall points</sub></td><td align="center" valign="top"><img src="../assets/images/drainage/retention-ponds.png" width="230" alt="Retention ponds"><br><sub>Retention ponds</sub></td></tr></table>

---

## Chapter 5 — Engineering the hydraulic model

The drainage representation was extended into an EPA SWMM 5.2.4 model.

The project reached a point where modelling was no longer just about generating layers; the computational system itself had to be debugged.

The workflow became:

```text
Build
 ↓
Simulate
 ↓
Diagnose
 ↓
Correct
 ↓
Rerun
 ↓
Verify
```

The model development included diagnosing numerical instability, correcting network geometry and slopes, regenerating the hydraulic model, rerunning simulations and verifying resulting outputs.

This engineering stage is important because the project became an iterative computational system rather than a static GIS analysis.

<table><tr><td align="center" valign="top"><img src="../assets/images/swmm/v7-3hr80-overview.png" width="310" alt="SWMM V7 (3 h): links by max depth / full depth, nodes by status"><br><sub>SWMM V7 (3 h): links by max depth / full depth, nodes by status</sub></td><td align="center" valign="top"><img src="../assets/images/swmm/flooded-nodes-200m-window.png" width="310" alt="200 m window on the flooded nodes"><br><sub>200 m window on the flooded nodes</sub></td></tr></table>

---

## Chapter 6 — From hydraulic response to flood depth

The next problem was translating hydraulic behaviour into a spatially understandable flood representation.

The project connected hydraulic outputs with GIS layers to produce flood-depth and inundation-oriented products.

The conceptual chain became:

```text
Hydraulic response
       ↓
Node / link outputs
       ↓
Spatial representation
       ↓
Flood depth
       ↓
Inundation
```

Now the model was answering a more practical question:

> **Where does the hydraulic response become visible flooding?**

<table><tr><td align="center" valign="top"><img src="../assets/images/inundation/flood-depth.png" width="440" alt="Flood depth (m), 0.02 to 1.58 m"><br><sub>Flood depth (m), 0.02 to 1.58 m</sub></td></tr></table>

---

## Chapter 7 — From flood maps to consequences

A flood map is useful.

But a decision-support system needs to go one step further.

The question became:

> **What does flood depth mean for movement through the city?**

This led to the road-accessibility layer, using depth thresholds of:

- 15 cm
- 30 cm
- 50 cm

The conceptual transition was:

```text
Flood depth
 ↓
Threshold
 ↓
Road impact
 ↓
Accessibility information
 ↓
Decision support
```

The system therefore moved from describing flood behaviour to translating it into an operationally meaningful consequence.

<table><tr><td align="center" valign="top"><img src="../assets/images/road-accessibility/impassable-15cm.png" width="230" alt="Impassable at 0.15 m"><br><sub>Impassable at 0.15 m</sub></td><td align="center" valign="top"><img src="../assets/images/road-accessibility/impassable-30cm.png" width="230" alt="Impassable at 0.30 m"><br><sub>Impassable at 0.30 m</sub></td><td align="center" valign="top"><img src="../assets/images/road-accessibility/impassable-50cm.png" width="230" alt="Impassable at 0.50 m"><br><sub>Impassable at 0.50 m</sub></td></tr></table>

---

## Chapter 8 — The SIH transition

When SIH 2026 presented the Urban Flood Nowcasting System problem, the project already had a hydro-spatial and hydraulic foundation.

The opportunity was therefore not to invent a flood project from scratch.

The direction became:

```text
Existing hydro-spatial foundation
          +
Drainage / hydraulic modelling
          +
Inundation / road impact
          ↓
SIH 2026 Nowcasting-oriented workflow
```

The broader objective became connecting rainfall/scenario information with terrain response, drainage hydraulics, inundation and road accessibility in one decision-support system.

<table><tr><td align="center" valign="top"><img src="../assets/images/overview/pipeline-montage.png" width="440" alt="Pipeline montage: DEM, flow accumulation, waterlogging risk, drainage network, SWMM result, inundation depth, impassable edges"><br><sub>Pipeline montage: DEM, flow accumulation, waterlogging risk, drainage network, SWMM result, inundation depth, impassable edges</sub></td></tr></table>

---

## The story in one line

> **Where does water go? → How does the drainage system respond? → Where does flooding appear? → Which roads are affected? → How can this become actionable flood intelligence?**

That sequence is the conceptual spine of NagarBadh Drishtm.

---

## What the story does not claim

The project story is intentionally not the same thing as a publication claim.

The associated manuscript covers only an earlier research stage.

The current repository documents a broader implementation that includes subsequent engineering and modelling work.

This distinction is maintained throughout the repository so that the project history, the research manuscript and the current software/dashboard are not conflated.
