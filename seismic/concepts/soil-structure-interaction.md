---
title: Soil-structure interaction
created: 2026-04-23
updated: 2026-04-23
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
---

# Soil-structure interaction

Soil-structure interaction (SSI) captures the two-way coupling between structural response, foundation compliance, and wave propagation in the supporting medium. In this batch SSI appears as a major theme linking practical finite element modeling, boundary treatment, and nuclear-structure applications.

## Why it matters

- SSI can alter effective stiffness, damping, kinematic input, and force transfer.
- Deeply embedded or heavy structures are especially sensitive to how soil pressures and wave transmission are modeled.
- SSI assumptions strongly influence the credibility of [[absorbing-and-transmitting-boundaries]] and [[nuclear-facility-seismic-analysis-and-design-criteria]].

## Evidence from this ingest batch

- The Tongji papers apply three-dimensional time-domain FE analysis to dynamic SSI for practical structures and tall buildings.
- The Brookhaven/NRC paper focuses on seismic-induced soil pressures on deeply embedded nuclear structures.
- Boundary-condition papers reinforce that SSI is inseparable from how the truncated soil domain is handled numerically.

## Engineering takeaway

SSI is not just a correction factor. It is a modeling regime with its own assumptions about foundation idealization, constitutive behavior, and radiation damping. When those assumptions are crude, the apparent precision of a large FE model can be misleading.

## Related

- [[absorbing-and-transmitting-boundaries]]
- [[rayleigh-damping-in-seismic-analysis]]
- [[nuclear-facility-seismic-analysis-and-design-criteria]]
- [[modal-combination-methods-and-floor-response-spectra]]
