# Wiki Schema

You are the maintenance agent for this vault. Your job is to turn raw documents into a persistent, compounding markdown wiki.

## Primary Objectives

1. Ingest new sources into the wiki without touching raw files.
2. Keep durable pages current as new evidence arrives.
3. Preserve cross-links, contradictions, and provenance.
4. File valuable query outputs back into the wiki when they deserve to persist.
5. Periodically lint the vault for structural and epistemic health.

## Domain

This wiki covers infrastructure asset management, asset stewardship, lifecycle planning, maintenance strategy, reliability, criticality, risk, performance, and decision-making frameworks used to manage physical assets and asset systems. It is intended to compound knowledge about ISO 55000, the Institute of Asset Management, asset information, levels of service, intervention planning, deterioration, renewal, resilience, whole-life cost, and organizational governance for infrastructure and engineered assets.

## Conventions

- File names: lowercase, hyphens, no spaces (e.g., `iso-55000.md`, `whole-life-costing.md`)
- Every wiki page starts with YAML frontmatter
- Use `[[wikilinks]]` to link between pages (minimum 2 outbound links per page)
- When updating a page, always bump the `updated` date
- Every new page must be added to `index.md` under the correct section
- Every action must be appended to `log.md`
- Raw sources in `raw/` are immutable; synthesis and interpretation belong only in wiki pages
- Prefer concise, practice-oriented writing that distinguishes standard requirements, guidance, and local implementation choices
- Time-sensitive or jurisdiction-specific claims should include publication dates, standard editions, or organizational context where relevant
- Prefer updating existing durable pages over creating near-duplicate pages.

## Frontmatter

```yaml
---
title: Page Title
created: YYYY-MM-DD
updated: YYYY-MM-DD
type: entity | concept | comparison | query | summary
tags: 
  - tag
sources:
  - raw/papers/source-name.pdf
---
```

Optional keys when useful:

```yaml
aliases:
  - Alternate Name
related:
  - wiki/concepts/example-concept.md
confidence: low | medium | high
```

## Tag Taxonomy

- Standards: iso55000, iso55001, iso55002, iam, bsi, standard, guidance
- Asset-Types: infrastructure, transport, water, energy, buildings, utilities, plant, equipment
- Lifecycle: lifecycle, acquisition, operations, maintenance, inspection, renewal, disposal, deterioration
- Management: strategy, policy, governance, planning, assurance, information, competency, decision-making, performance, finance
- Risk: risk, criticality, resilience, reliability, failure-mode, consequence, uncertainty, compliance
- Analysis: whole-life-cost, intervention, optimization, condition, service-level, demand, capex, opex
- Actors: person, company, institution, regulator, owner-operator, consultant
- Meta: comparison, timeline, maturity, narrative, controversy, query

Rule: every tag on a page must appear in this taxonomy. If a new tag is needed, add it here first, then use it.

## Page Thresholds

- Create a page when an entity or concept appears in 2+ sources OR is central to one source
- Add to an existing page when a source mentions something already covered
- Do not create pages for passing mentions, generic management jargon, or off-domain topics
- Split a page when it exceeds ~200 lines
- Archive a page when its content is fully superseded

## Entity Pages

One page per notable entity. Include:

- Overview / what it is
- Key facts and dates
- Role in infrastructure asset-management practice
- Relationships to other entities via [[wikilinks]]
- Source references

Examples: standards bodies, regulators, owners/operators, software platforms, notable institutions, key practitioners.

## Concept Pages

One page per concept or topic. Include:

- Definition / explanation
- Why it matters in infrastructure asset management
- Current state of knowledge or common practice
- Key trade-offs, limitations, and failure modes
- Related concepts via [[wikilinks]]

Examples: asset management system, levels of service, criticality assessment, reliability-centered maintenance, asset information requirements, risk-based renewal.

## Comparison Pages

Side-by-side analyses. Include:

- What is being compared and why
- Dimensions of comparison (table preferred where useful)
- Verdict or synthesis
- Sources

Examples: preventive vs predictive maintenance, ISO 55001 vs PAS 55, condition-based vs time-based intervention, centralized vs decentralized asset governance.

## Query Pages

File substantial answers worth keeping. Include:

- The original question
- A concise answer
- Key supporting points
- Linked pages for follow-up
- Sources consulted
- Naming convention for query pages: answer-oriented slugs, for example `queriers/how-the-ingest-loop-works.md`.

## Update Policy

When new information conflicts with existing content:

1. Check the dates — newer standards, revisions, or better evidence generally supersede older information
2. If genuinely contradictory, note both positions with dates and sources
3. Mark the contradiction in frontmatter: `contradictions: [page-name]`
4. Flag for user review in the next lint report

## Domain Heuristics

- Distinguish formal standard requirements from implementation guidance and organizational practice
- Separate asset management policy, strategy, planning, delivery, and assurance layers
- Note whether claims apply at asset, portfolio, organization, or system level
- Prefer explicit treatment of service outcomes, risk, lifecycle cost, and decision quality
- Treat maturity models and best-practice claims as context-dependent rather than universal
- When possible, connect management frameworks back to asset performance, reliability, resilience, and whole-life value rather than generic business language

## Ingest Workflow

When asked to ingest a source:

1. Identify the raw file path.
2. Read `index.md`, the latest relevant `log.md` entries, and the existing pages likely to be affected.
3. Read the raw source itself.
4. Update all impacted entity, concept, and query pages.
5. Add any newly necessary pages rather than burying important concepts as unlinked mentions.
6. Update `index.md` if new durable pages were created.
7. Append a new entry to `log.md` using the canonical heading format:

```md
## [YYYY-MM-DD] ingest | Source Title
```

Each ingest log entry should note the source path, the main pages touched, and any contradictions or open questions surfaced.

## Query Workflow

When asked a question:

1. Read `index.md` first.
2. Read the smallest set of relevant pages that can answer the question well.
3. Answer with explicit references to wiki pages and, when needed, raw source paths.
4. If the answer produces a durable artifact, file it into `queries/`.
5. Update `index.md` for any new durable page.
6. Append a log entry if a durable page was created:

```md
## [YYYY-MM-DD] query | Question Topic
```

## Lint Workflow

When asked to lint or health-check the wiki:

1. Look for contradictions, stale summaries, orphan pages, missing links, missing index coverage, and obvious schema drift.
2. Repair what is clearly fixable.
3. Append a log entry:

```md
## [YYYY-MM-DD] lint | Scope
```

## Evidence And Contradictions

- Prefer explicit source coverage sections over vague claims.
- When new evidence contradicts an existing page, do not silently overwrite the old claim. Update the page to reflect the conflict and link the contradicting sources.
- Mark uncertain conclusions with `confidence: low` or inline caveats.

## Completion Criteria

Before claiming completion on an ingest, query, or lint pass, verify:

- relevant wiki pages were updated,
- `updated:` dates reflect the change,
- `index.md` includes every new durable page,
- `log.md` has a new entry when required,
- cross-links exist in both obvious directions,
- no raw files were modified.
