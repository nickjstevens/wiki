---
title: Nonstationary ground-motion generation and spectral matching
created: 2026-04-23
updated: 2026-04-23
type: concept
tags:
  - seismic
  - time-history
  - response-spectrum
  - dynamics
  - modeling
  - assumption
sources:
  - raw/papers/A stochastic approach for generating spectrum compatible fully nonstationary earthquakes.pdf
  - raw/papers/An Improved Method For Nonstationary Spectral Matching - RSPMATCH.pdf
---

# Nonstationary ground-motion generation and spectral matching

This topic covers procedures for generating acceleration histories that satisfy a target response spectrum while retaining realistic nonstationary behavior in amplitude and frequency content.

## Why it matters

- Nonlinear dynamic analysis needs records that are not merely spectrum-compatible but also physically defensible.
- Matching algorithms can hide unrealistic signal manipulation behind apparently good spectral agreement.
- The topic feeds directly into [[nonlinear-seismic-assessment-methods]] and [[seismic-hazard-assessment-for-nuclear-sites]].

## Evidence from this ingest batch

- Cacciola proposes a stochastic method aimed at fully nonstationary, code-compatible artificial earthquakes.
- The RSPMATCH paper presents an improved time-domain spectral matching approach for modifying existing accelerograms.

## Engineering takeaway

Spectral compatibility is necessary but not sufficient. Record selection and modification should preserve the aspects of time variation and frequency evolution that materially affect inelastic demand, cumulative damage, and tuning-sensitive subsystems.

## Related

- [[nonlinear-seismic-assessment-methods]]
- [[seismic-hazard-assessment-for-nuclear-sites]]
- [[modal-combination-methods-and-floor-response-spectra]]
