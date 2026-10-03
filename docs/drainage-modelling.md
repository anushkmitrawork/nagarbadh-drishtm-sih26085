# 💧 Drainage Modelling

## Why a drainage model?

Terrain explains surface behaviour, but urban flooding is also controlled by engineered drainage infrastructure.

The project therefore represents drainage as an explicit computational network.

## Current representation

The model documentation includes:

- **28,370 drainage conduit segments**
- Nodes
- Outfalls
- Retention ponds
- Intervention zones
- Hydraulic test/analysis layers

## Network concept

```text
Rainfall / runoff
      ↓
Drainage nodes
      ↓
Conduits
      ↓
Outfalls / storage
      ↓
Hydraulic response
```

The drainage network becomes the bridge between hydro-spatial analysis and hydraulic simulation.

---

## Next layer

The drainage representation is simulated using EPA SWMM 5.2.4.

See [Hydraulic Modelling](hydraulic-modelling.md).
