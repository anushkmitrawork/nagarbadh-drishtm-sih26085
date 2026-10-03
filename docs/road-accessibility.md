# 🚧 Road Accessibility

## Why road impact matters

Flood depth is a physical quantity.

For emergency response, transport and urban management, the more practical question is:

> **Which roads are affected at a given flood depth?**

The project therefore converts flood depth into threshold-based road-accessibility layers.

## Thresholds

- **15 cm**
- **30 cm**
- **50 cm**

## Workflow

```text
Flood-depth surface
        ↓
Threshold classification
        ↓
Road / edge impact
        ↓
Accessibility information
        ↓
Decision support
```

This layer turns flood modelling into an operationally interpretable output.

---

## Why this matters

The system therefore goes beyond:

> **Where will water accumulate?**

toward:

> **Which movement corridors become affected?**

---

## Figures: impassable edges by threshold

<p align="center"><img src="../assets/images/road-accessibility/impassable-15cm.png" width="560" alt="Impassable at 0.15 m"><br><sub><b>Impassable edges at 0.15 m.</b></sub></p>
<p align="center"><img src="../assets/images/road-accessibility/impassable-30cm.png" width="560" alt="Impassable at 0.30 m"><br><sub><b>Impassable edges at 0.30 m.</b></sub></p>
<p align="center"><img src="../assets/images/road-accessibility/impassable-50cm.png" width="560" alt="Impassable at 0.50 m"><br><sub><b>Impassable edges at 0.50 m.</b></sub></p>
