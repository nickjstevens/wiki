---
title: Absorbing and transmitting boundaries
created: 2026-04-23
updated: 2026-04-23
type: concept
tags:
  - seismic
  - modeling
  - dynamics
  - geotechnical
  - time-history
  - limitation
sources:
  - raw/papers/A Unified Viscous-SpringArtificial Boundary for 3D Static and Dynamic Applications (TransmittingBoundaries).pdf
  - raw/papers/Absorbing Boundary Conditions for Seismic Analysis in ABAQUS - Nielson - 2006.pdf
  - raw/papers/Local transmitting boundaries for transient elastic analysis - Kellezi - 2000.pdf
  - raw/papers/Modeling Methods for Silent Boundaries in Infinite Media - Ross - 2004.pdf
---

# Absorbing and transmitting boundaries

Absorbing or transmitting boundaries are numerical devices used to truncate semi-infinite media without reflecting unrealistic wave energy back into the finite model. They matter whenever seismic wave propagation, soil domains, or foundation interaction are modeled explicitly.

## Why it matters

- Artificial reflections can contaminate demand estimates, especially in time-domain analyses.
- Boundary formulation controls whether a local finite element model behaves like a bounded box or a piece of an unbounded continuum.
- The choice is tightly coupled to [[soil-structure-interaction]] and to software implementation details in [[nuclear-facility-seismic-analysis-and-design-criteria]].

## Evidence from this ingest batch

- Liu and Li present a unified viscous-spring artificial boundary intended to serve both static and dynamic applications.
- Nielsen's ABAQUS paper reviews practical absorbing boundary condition options and then derives a user element implementation for seismic analysis.
- Kellezi focuses on local transmitting boundaries for transient elastic SSI-style problems.
- Ross surveys silent-boundary modeling options for infinite-media approximations.

## Engineering takeaway

The recurring theme is not that one boundary is universally best, but that boundary choice must match the governing physics, the solver's formulation, and the desired balance between practicality and wave-absorption fidelity.

## Common limitations

- Good absorption in one frequency range may not generalize cleanly across all motions.
- Easy-to-implement local boundaries can be attractive, but they often trade some rigor for practicality.
- Boundary quality cannot rescue an overly crude soil constitutive model or mesh.

## Related

- [[soil-structure-interaction]]
- [[rayleigh-damping-in-seismic-analysis]]
- [[nuclear-facility-seismic-analysis-and-design-criteria]]
