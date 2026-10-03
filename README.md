# 🌊 NagarBadh Drishtm

## From a Second-Semester MCA Project to an Urban Flood Intelligence System

**SIH 2026 · SIH26085 · Urban Flood Nowcasting System · Disaster Management**

[🌐 Open Live Dashboard](https://anushkmitrawork.github.io/nagarbadh-drishtm-sih26085/) · [📖 Project Story](docs/project-story.md) · [🧭 Methodology](docs/methodology.md) · [📚 Research & Literature](docs/research-literature.md)

---

## The story

**NagarBadh Drishtm did not begin as a Smart India Hackathon idea.**

It began as a second-semester MCA project exploring how terrain, hydrology and spatial analysis could be used to understand urban waterlogging.

The first question was:

> **Where does water go?**

As the modelling developed, the question became deeper:

> **How does the drainage system respond?**

That led to detailed drainage representation and SWMM-based hydraulic modelling.

The work subsequently expanded through CIIAR at DES Pune University and into 3D computational modelling, where the GIS environment was translated into a geographically accurate 3D representation for collaboration with a Unity development team.

The next questions became:

> **Where does hydraulic stress become surface flooding?**

and

> **Which roads become inaccessible?**

SIH 2026 became the next evolution: extending the hydro-spatial and hydraulic foundation toward an urban flood nowcasting and decision-support workflow.

---

## 🧭 Project evolution

**Second-Semester MCA Project**  
Terrain + hydrology + waterlogging

↓

**Hydro-spatial research**  
Terrain-derived hydrological and risk analysis

↓

**CIIAR / DES Pune University**  
Research expansion and computational modelling

↓

**3D computational modelling**  
Geographically accurate 3D environment for Unity collaboration

↓

**Drainage + SWMM**  
Detailed drainage representation and hydraulic simulation

↓

**Inundation + road accessibility**  
Flood depth translated into practical road-impact layers

↓

**SIH 2026**  
Urban flood nowcasting and decision support

---

## 🧠 Three representations of the problem

| Representation | Question |
|---|---|
| 🗺️ **Analytical GIS** | Where does water go? |
| ⚙️ **Hydraulic SWMM** | How does the drainage system respond? |
| 🚨 **Decision Support** | What does flooding mean operationally? |

---

## ⚙️ Computational pipeline

```text
Rainfall / Scenario
       ↓
Terrain
       ↓
Hydrology
       ↓
Drainage Network
       ↓
SWMM Hydraulic Simulation
       ↓
Flood Depth
       ↓
15 / 30 / 50 cm Thresholds
       ↓
Road Accessibility
       ↓
Decision Support
       ↓
Interactive Dashboard
```

---

## 📊 Current system snapshot

- **54 GIS layers**
- **10 km Pune urban study area**
- **28,370 drainage conduit segments**
- **EPA SWMM 5.2.4 / PySWMM**
- **PostgreSQL + PostGIS**
- **QGIS / PyQGIS**
- **Event/scenario inundation products**
- **15 / 30 / 50 cm road-accessibility thresholds**
- **Interactive web dashboard**

---

## 🖥️ Explore the working system

### Live Dashboard

The repository's existing `index.html` is the deployed NagarBadh Drishtm dashboard.

**[🌐 Open the live dashboard →](https://anushkmitrawork.github.io/nagarbadh-drishtm-sih26085/)**

The dashboard is the deployed product; the repository documentation below provides the research and engineering record behind it.

### Project documentation

- [Project Story](docs/project-story.md)
- [Project Origin](docs/project-origin.md)
- [Research Evolution](docs/research-evolution.md)
- [Methodology](docs/methodology.md)
- [System Architecture](docs/system-architecture.md)
- [Geospatial Modelling](docs/geospatial-modelling.md)
- [Drainage Modelling](docs/drainage-modelling.md)
- [Hydraulic Modelling](docs/hydraulic-modelling.md)
- [Inundation Modelling](docs/inundation-modelling.md)
- [Road Accessibility](docs/road-accessibility.md)
- [Dashboard Documentation](docs/dashboard.md)
- [Data & References](docs/data-and-references.md)
- [Research Literature](docs/research-literature.md)
- [Publication Status](docs/publication-status.md)
- [Future Work](docs/future-work.md)

---

## 🔬 Research and publication status

The associated manuscript represents **one stage of the broader project** and is currently **unpublished**.

Its scope is primarily the earlier hydro-spatial research foundation. The current NagarBadh Drishtm implementation has subsequently expanded beyond that manuscript into drainage-network modelling, SWMM hydraulics, event/scenario inundation, road-accessibility analysis and the SIH-oriented nowcasting workflow.

The repository therefore documents the **broader project evolution and implementation**, while the manuscript remains a distinct research output with its own scope.

See [Publication Status](docs/publication-status.md) and [Research & Literature](docs/research-literature.md).

---

## 🔭 Future research direction

Possible future development includes:

- Automated rainfall / nowcast ingestion
- Automated rainfall-to-hydraulic-model forcing
- Continuous hydraulic simulation
- Higher-resolution inundation modelling
- Operational database updates
- Navigation / flood-safe routing integration
- Further 3D digital-twin development
- Formal publication of the associated research

Future work is documented separately so that planned capabilities are not confused with the current implementation.

---

## 📌 Scope note

This repository is a **research and engineering record** as well as a dashboard repository.

The story describes the project's evolution.  
The technical documents describe the implemented modelling workflow.  
The literature section links external published research.  
The associated manuscript is clearly identified as unpublished and limited to its own scope.

`index.html` remains the live dashboard entry point.
