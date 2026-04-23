---
title: 2026-04-23 seismic raw batch triage
created: 2026-04-23
updated: 2026-04-23
type: query
tags:
  - seismic
  - query
  - assumption
  - limitation
sources:
  - raw/papers/ASCE 4-16_ocr.pdf
  - raw/papers/Seismic Analysis of Safety-Related Nuclear Structures - 2017.pdf
---

# 2026-04-23 seismic raw batch triage

## Question

What did this first raw-paper sync add, and are there any obvious curation issues?

## Answer

The batch establishes a strong starting spine for the seismic wiki around nuclear standards, SSI and wave-boundary modeling, nonlinear assessment methods, steel seismic design, and selected RC and isolation topics. One curation issue surfaced immediately:

1. `Seismic Analysis of Safety-Related Nuclear Structures - 2017.pdf` appears to duplicate the ASCE/SEI 4-16 standard already present as `ASCE 4-16_ocr.pdf`.

## Key supporting points

- Nuclear standards and workflows are now represented by [[asce-sei-4-16]], [[asce-sei-43-05]], and [[nuclear-facility-seismic-analysis-and-design-criteria]].
- Wave-boundary and SSI modeling are represented by [[absorbing-and-transmitting-boundaries]] and [[soil-structure-interaction]].
- Nonlinear assessment and design-method topics are represented by [[nonlinear-seismic-assessment-methods]], [[pushover-analysis-for-seismic-assessment]], and [[seismic-design-of-steel-moment-frames]].

## Follow-up

- If desired, split future ingest batches by subdomain to deepen each page with clause-level or method-level detail.
