---
title: Soil-structure interaction
created: 2026-04-23
updated: 2026-04-24
type: concept
tags:
  - seismic
  - geotechnical
  - dynamics
  - modeling
  - foundation
  - time-history
sources:
  - raw/papers/Computer simulation on dynamic soil-structure interaction system - 2004.pdf
  - raw/papers/Numerical Analysis of Tall Buildings Considering Dynamic Soil-Structure Interaction - 2003.pdf
  - raw/papers/Finite Element Models for Computing Seismic Induced Soil Pressures on Deeply Embedded Nuclear Power Plant Structures.pdf
  - raw/papers/Absorbing Boundary Conditions for Seismic Analysis in ABAQUS - Nielson - 2006.pdf
  - raw/papers/Local transmitting boundaries for transient elastic analysis - Kellezi - 2000.pdf
  - raw/articles/2026-04-22-kahramanmaras-soil-structure-interaction-resonance-study.md
  - raw/articles/2026-04-23-train-bridge-pile-soil-interaction-and-pile-base-response.md
---

# Soil-structure interaction

Soil-structure interaction (SSI) captures the two-way coupling between structural response, foundation compliance, and wave propagation in the supporting medium. The existing nuclear-oriented material in this wiki already showed why SSI matters; this week's sources sharpen that lesson with two reminders: resonance checks based only on dominant period can miss the governing demand case, and coupled moving-load-plus-earthquake problems can amplify pile and foundation demands in non-intuitive ways.

## Why it matters

- SSI can alter effective stiffness, damping, kinematic input, and force transfer.
- Deeply embedded or heavy structures are especially sensitive to how soil pressures and wave transmission are modeled.
- Mid-rise buildings and supported infrastructure can see higher demand even when the obvious soil-period resonance story looks manageable.
- SSI assumptions strongly influence the credibility of [[absorbing-and-transmitting-boundaries]] and [[nuclear-facility-seismic-analysis-and-design-criteria]].

## Evidence from this ingest batch

- The earlier Tongji and Brookhaven/NRC material established SSI as a core modeling regime for practical and nuclear structures.
- Güllü and Natur (2026) show that building demand under the 2023 Kahramanmaraş-Pazarcık motion did not reduce to a simple “avoid the resonance period” rule: the 4-storey case aligned most closely with the dominant soil period, but the 7-storey building developed the highest rocking, base shear, and drift demand on the studied soft-soil profile.
- Xie et al. (2026) extend SSI into a coupled train–bridge–pile–soil setting, where moving loads and earthquake input interact nonlinearly and broaden the effective response band at the pile base.
- The new bridge paper also reinforces that SSI quality depends on boundary treatment; viscoelastic absorbing boundaries were necessary to represent wave radiation and avoid misleading pile-base demand histories.

## Engineering takeaway

SSI is not just a correction factor. It is a modeling regime with its own assumptions about foundation idealization, constitutive behavior, boundary truncation, and coupled loading. Simple period-matching heuristics are useful for screening, but they are not enough to identify the controlling demand case when soft soil, rocking, or additional dynamic systems are present.

## Related

- [[absorbing-and-transmitting-boundaries]]
- [[bridge-pile-soil-interaction-under-seismic-and-moving-loads]]
- [[rayleigh-damping-in-seismic-analysis]]
- [[nuclear-facility-seismic-analysis-and-design-criteria]]
- [[modal-combination-methods-and-floor-response-spectra]]
