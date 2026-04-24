# Wiki Log

> Chronological record of all wiki actions. Append-only.
> Format: `## [YYYY-MM-DD] action | subject`
> Actions: ingest, update, query, lint, create, archive, delete
> When this file exceeds 500 entries, rotate: rename to log-YYYY.md, start fresh.

## [2026-04-17] create | Wiki initialized

- Domain: Seismic analysis and design
- Path: /home/nick/Documents/wiki/seismic
- Structure created with SCHEMA.md, index.md, log.md
- Directories created: raw/articles, raw/papers, raw/transcripts, raw/assets, entities, concepts, comparisons, queries

## [2026-04-23] ingest | Initial seismic raw-paper batch

- Sources reviewed: 29 new PDFs under `raw/papers/`
- Durable pages created: `entities/asce-sei-4-16.md`, `entities/asce-sei-43-05.md`, `entities/aisc-341-05.md`, `entities/aisc-358-05.md`, `entities/nist-gcr-10-917-5.md`, `concepts/absorbing-and-transmitting-boundaries.md`, `concepts/soil-structure-interaction.md`, `concepts/nonstationary-ground-motion-generation-and-spectral-matching.md`, `concepts/pushover-analysis-for-seismic-assessment.md`, `concepts/seismic-design-of-steel-moment-frames.md`, `concepts/nonlinear-seismic-assessment-methods.md`, `concepts/base-isolation-with-friction-pendulum-systems.md`, `concepts/rayleigh-damping-in-seismic-analysis.md`, `concepts/modal-combination-methods-and-floor-response-spectra.md`, `concepts/nuclear-facility-seismic-analysis-and-design-criteria.md`, `concepts/seismic-hazard-assessment-for-nuclear-sites.md`, `concepts/reinforced-concrete-vulnerability-and-progressive-collapse.md`, `queries/2026-04-23-seismic-raw-batch-triage.md`
- Main themes ingested: nuclear seismic standards, SSI and wave-boundary modeling, nonlinear assessment methods, steel seismic design, damping, floor spectra, base isolation, and RC vulnerability.
- Triage notes: duplicate ASCE 4-16 raw files were identified during ingest; cleanup completed in the update entry below.

## [2026-04-23] update | ASCE 4-16 duplicate raw-file cleanup

- Removed duplicate raw source: `raw/papers/Seismic Analysis of Safety-Related Nuclear Structures - 2017.pdf`
- Retained the better-named canonical copy: `raw/papers/ASCE 4-16 - Seismic Analysis of Safety-Related Nuclear Structures.pdf`
- Updated wiki source references to the canonical filename across entity, concept, query, and log files

## [2026-04-24] ingest | Weekly seismic research scan

- Sources added: `raw/articles/2026-04-22-kahramanmaras-soil-structure-interaction-resonance-study.md`, `raw/articles/2026-04-23-train-bridge-pile-soil-interaction-and-pile-base-response.md`, `raw/articles/2026-04-22-concrete-microcracks-under-seismic-strain-rates.md`
- Durable pages created: `concepts/bridge-pile-soil-interaction-under-seismic-and-moving-loads.md`, `concepts/concrete-microcracking-and-rate-effects-under-seismic-loading.md`, `queries/2026-04-24-weekly-seismic-research-scan.md`
- Durable pages updated: `concepts/soil-structure-interaction.md`, `concepts/reinforced-concrete-vulnerability-and-progressive-collapse.md`, `index.md`
- Main themes: SSI demand beyond simple resonance heuristics, coupled train–bridge–pile–soil dynamics, and brittle fracture implications hidden beneath concrete rate effects.
- UK nuclear-specific result: no clearly on-point UK nuclear seismic publication found within the search window; broader methodological relevance noted in the weekly query page.
