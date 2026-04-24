# Wiki Log

> Chronological record of all wiki actions. Append-only.
> Format: `## [YYYY-MM-DD] action | subject`
> Actions: ingest, update, query, lint, create, archive, delete
> When this file exceeds 500 entries, rotate: rename to log-YYYY.md, start fresh.

## [2026-04-17] create | Wiki initialized

- Domain: Asset management
- Path: /home/nick/Documents/wiki/asset-management
- Structure created with SCHEMA.md, index.md, log.md
- Directories created: raw/articles, raw/papers, raw/transcripts, raw/assets, entities, concepts, comparisons, queries

## [2026-04-17] update | Domain corrected

- Clarified that this wiki is for infrastructure asset management, not investing, trading, or fund management
- Updated: SCHEMA.md

## [2026-04-17] ingest | iam-anatomy-version-4-final

- Source analyzed: raw/papers/iam-anatomy-version-4-final.pdf
- Added pages:
  - entities/institute-of-asset-management.md
  - concepts/asset-management.md
  - concepts/line-of-sight.md
  - concepts/iam-10-box-capabilities-model.md
  - concepts/asset-management-system.md
  - concepts/asset-management-decision-making.md
  - concepts/risk-management.md
  - concepts/value-realization.md
- Updated: index.md

## [2026-04-22] ingest | Batch ingest of new asset-management source files

- Normalized raw source filenames:
  - raw/papers/big-data-analytical-architecture-for-asset-management-2017.pdf
  - raw/papers/physical-asset-management-core-practices-operational-performance-2020.pdf
  - raw/papers/iaea-asset-management-for-sustainable-nuclear-power-plant-operation-2021.pdf
  - raw/papers/project-routemap-asset-management-handbook-2022.pdf
  - raw/papers/whole-life-management-of-physical-assets-2010.pdf
  - raw/papers/iso-55000-2024.pdf
  - raw/papers/iso-55001-2024.pdf
  - raw/papers/iso-55002-2018.pdf
  - raw/papers/gfmam-asset-management-landscape-2024.pdf
  - raw/papers/gfmam-digital-transformation-in-maintenance-and-asset-management-2024.pdf
  - raw/papers/gfmam-asset-management-maturity-position-statement-2021.pdf
  - raw/papers/iaea-tecdoc-1590-reliability-centred-maintenance-2008.pdf
  - raw/papers/insag-25-integrated-risk-informed-decision-making-2011.pdf
  - raw/papers/epri-nuclear-asset-management-toolkit-definition-and-industry-survey-2006.pdf
  - raw/papers/pas-55-1-2008.pdf
  - raw/papers/physical-asset-management-hastings-2010.pdf
  - raw/papers/construction-playbook-2020.pdf
  - raw/papers/onr-ns-tast-gd-098-asset-management-guide-2022.docx
- Added pages:
  - entities/british-standards-institution.md
  - entities/global-forum-on-maintenance-and-asset-management.md
  - entities/international-atomic-energy-agency.md
  - entities/office-for-nuclear-regulation.md
  - concepts/iso-55000.md
  - concepts/iso-55001.md
  - concepts/iso-55002.md
  - concepts/pas-55.md
  - concepts/asset-management-maturity.md
  - concepts/digital-transformation-in-asset-management.md
  - concepts/physical-asset-management.md
  - concepts/lifecycle-delivery.md
  - concepts/asset-information.md
  - concepts/asset-review.md
  - concepts/reliability-centered-maintenance.md
  - concepts/nuclear-asset-management.md
- Updated pages:
  - entities/institute-of-asset-management.md
  - concepts/asset-management.md
  - concepts/asset-management-system.md
  - concepts/asset-management-decision-making.md
  - concepts/iam-10-box-capabilities-model.md
  - concepts/risk-management.md
  - index.md
- Source themes integrated: ISO 55000 series, PAS 55, GFMAM landscape and maturity, digital transformation, physical asset management, lifecycle delivery, nuclear asset management, and reliability-centered maintenance

## [2026-04-24] ingest | Weekly asset-management research ingest

- Research window checked: 2026-04-17 through 2026-04-24 UTC
- New standards / IAM / formal guidance found in-window: none confirmed
- Added raw sources:
  - raw/papers/quasi-experimental-efficiency-diagnostics-nigerian-municipal-infrastructure-asset-management-2026.pdf
  - raw/papers/ar-mr-equipment-for-physical-asset-management-applications-2026.pdf
- Updated pages:
  - concepts/digital-transformation-in-asset-management.md
  - concepts/asset-management-decision-making.md
  - concepts/physical-asset-management.md
- Notes:
  - The Nigerian municipal infrastructure paper is an abstract-only publication that introduces a quasi-experimental evaluation framework rather than reporting field results.
  - The AR/MR paper adds current practice guidance on device selection, ruggedisation, offline work, and workflow integration for physical asset management.
