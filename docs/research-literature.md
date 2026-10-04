# 📖 Research & Literature

## Purpose

This section collects **external published research and technical literature** relevant to the scientific and engineering foundations of NagarBadh Drishtm.

It is intentionally separate from the project's own unpublished manuscript.

### How to read this list

- Each entry is an **external, published work**. Listing a paper means it is relevant background, not that the project reproduces its method or endorses every conclusion.
- The one-line *relevance* notes describe how the paper relates to a part of the project. Where the project does something different (for example a simpler classification than the paper uses), the note says so.
- Citation details (authors, year, venue, DOI) were checked against publisher or repository records. Please re-check a DOI before citing it in formal work.
- The consolidated, citation-style list is in the [Bibliography](../references/bibliography.md).

---

## 1. Urban Flood Modelling

Literature on:

- Urban hydrological modelling
- GIS-based flood assessment
- Surface runoff and urban waterlogging
- Flood-risk mapping

**Selected references**

- **Beven, K. J., & Kirkby, M. J. (1979).** A physically based, variable contributing area model of basin hydrology. *Hydrological Sciences Bulletin*, 24(1), 43–69. [doi:10.1080/02626667909491834](https://doi.org/10.1080/02626667909491834)  
  *Relevance:* introduced the topography-driven contributing-area idea (upslope area relative to local slope) from which the topographic wetness index is derived; the conceptual basis for the TWI layer in the hydro-spatial model.

---

## 2. Urban Drainage & SWMM

Literature on:

- EPA SWMM applications
- Urban drainage-network modelling
- Hydraulic capacity
- Surcharge and flooding
- Drainage-system decision support

**Selected references**

- **Niazi, M., Nietch, C., Maghrebi, M., Jackson, N., Bennett, B. R., Tryby, M., & Massoudieh, A. (2017).** Storm water management model: Performance review and gap analysis. *Journal of Sustainable Water in the Built Environment*, 3(2), 04017002. [doi:10.1061/JSWBAY.0000817](https://doi.org/10.1061/JSWBAY.0000817)  
  *Relevance:* reviews how SWMM has been calibrated and validated in the peer-reviewed literature and identifies gaps; useful context for the verification steps and stated limitations of the project's SWMM workflow.

- **Bisht, D. S., Chatterjee, C., Kalakoti, S., Upadhyay, P., Sahoo, M., & Panda, A. (2016).** Modeling urban floods and drainage using SWMM and MIKE URBAN: a case study. *Natural Hazards*, 84, 749–776. [doi:10.1007/s11069-016-2455-1](https://doi.org/10.1007/s11069-016-2455-1)  
  *Relevance:* an Indian example of applying SWMM to an urbanised catchment, including design-storm estimation and drainage design.

---

## 3. Rainfall & Nowcasting

Literature on:

- Doppler-weather-radar rainfall nowcasting
- Short-term rainfall prediction
- Rainfall–runoff coupling
- High-resolution rainfall forcing

> **Scope note:** these papers describe nowcasting *methods*. The current NagarBadh Drishtm implementation uses event/scenario rainfall; automated nowcast ingestion is listed under [Future Work](future-work.md).

**Selected references**

- **Shi, X., Chen, Z., Wang, H., Yeung, D.-Y., Wong, W.-K., & Woo, W.-C. (2015).** Convolutional LSTM network: A machine learning approach for precipitation nowcasting. *Advances in Neural Information Processing Systems 28 (NIPS 2015)*, 802–810. [NeurIPS](https://proceedings.neurips.cc/paper/2015/hash/07563a3fe3bbe7e3ba84431ad9d055af-Abstract.html) · [arXiv:1506.04214](https://arxiv.org/abs/1506.04214)  
  *Relevance:* formulates precipitation nowcasting as a spatiotemporal sequence-forecasting problem; an early deep-learning reference for short-term rainfall prediction.

- **Ravuri, S., Lenc, K., Willson, M., et al. (2021).** Skilful precipitation nowcasting using deep generative models of radar. *Nature*, 597(7878), 672–677. [doi:10.1038/s41586-021-03854-z](https://doi.org/10.1038/s41586-021-03854-z)  
  *Relevance:* probabilistic radar-based nowcasting up to about two hours ahead; indicates what a future rainfall-forcing stage for the flood workflow could draw on.

- **Pulkkinen, S., Nerini, D., Hortal, A. A. P., et al. (2019).** Pysteps: an open-source Python library for probabilistic precipitation nowcasting (v1.0). *Geoscientific Model Development*, 12(10), 4185–4219. [doi:10.5194/gmd-12-4185-2019](https://doi.org/10.5194/gmd-12-4185-2019)  
  *Relevance:* open-source, Python-based probabilistic nowcasting framework, which fits naturally with the project's Python/PySWMM tooling if automated rainfall forcing is added.

---

## 4. Flood Inundation

Literature on:

- Flood-depth modelling
- 1D / 2D hydraulic modelling
- Inundation mapping
- High-resolution urban flood representation

**Selected references**

- **Teng, J., Jakeman, A. J., Vaze, J., Croke, B. F. W., Dutta, D., & Kim, S. (2017).** Flood inundation modelling: A review of methods, recent advances and uncertainty analysis. *Environmental Modelling & Software*, 90, 201–216. [Record (ANU)](https://researchportalplus.anu.edu.au/en/publications/flood-inundation-modelling-a-review-of-methods-recent-advances-an/)  
  *Relevance:* reviews empirical, hydrodynamic and simple conceptual inundation models and their uncertainty; a reference point for positioning the project's drainage-driven flood-depth products against other model families.

---

## 5. GIS-Based Decision Support

Literature on:

- Emergency response
- Road accessibility under flood conditions
- Urban resilience
- GIS decision-support systems

**Selected references**

- **Pregnolato, M., Ford, A., Wilkinson, S. M., & Dawson, R. J. (2017).** The impact of flooding on road transport: A depth-disruption function. *Transportation Research Part D: Transport and Environment*, 55, 67–81. [doi:10.1016/j.trd.2017.06.020](https://doi.org/10.1016/j.trd.2017.06.020)  
  *Relevance:* relates standing-water depth to vehicle speed and argues that treating a road as simply open or blocked is not supported by observation. The project's 15 / 30 / 50 cm impassability thresholds are a simpler, classification-style representation of this depth–disruption idea, not a reproduction of the function.

- **Pregnolato, M., Ford, A., Glenis, V., Wilkinson, S., & Dawson, R. (2017).** Impact of climate change on disruption to urban transport networks from pluvial flooding. *Journal of Infrastructure Systems*, 23(4), 04017015. [doi:10.1061/(ASCE)IS.1943-555X.0000372](https://doi.org/10.1061/(ASCE)IS.1943-555X.0000372)  
  *Relevance:* couples pluvial flood simulation with transport analysis and uses a criticality index to prioritise interventions; an example of turning flood depth into road-network consequences.

---

## 6. Indian Urban Flood Systems

Relevant research and operational systems concerning Indian urban flooding, including work connected to rainfall, urban drainage, flood modelling and decision support.

**Selected references**

- **Sonavane, N., et al. (2020).** Urban storm-water modeling using EPA SWMM — a case study of Pune city. Conference paper. [doi:10.1109/B-HTC50970.2020.9297900](https://doi.org/10.1109/B-HTC50970.2020.9297900)  
  *Relevance:* SWMM-based stormwater modelling for Pune, the same city as the project's study area.

- **Gupta, K. (2007).** Urban flood resilience planning and management and lessons for the future: A case study of Mumbai, India. *Urban Water Journal*, 4(3), 183–194. [doi:10.1080/15730620701464141](https://doi.org/10.1080/15730620701464141)  
  *Relevance:* describes Mumbai's drainage system, the 2005 flooding and mitigation measures; a widely cited Indian case for urban flood resilience planning.

- **Bisht et al. (2016)** — see [Section 2](#2-urban-drainage--swmm).

_Operational Indian sources (for example IMD and NCMRWF rainfall products) are not yet catalogued here and can be added as they are consulted._

---

## Adding the project's own manuscript

The associated manuscript should not be listed as a published paper.

See [Publication Status](publication-status.md) for its current scope and status.
