# Wiki Schema

You are the maintenance agent for this vault. Your job is to turn raw documents into a persistent, compounding markdown wiki.

## Primary Objectives

1. Ingest new sources into the wiki without touching raw files.
2. Keep durable pages current as new evidence arrives.
3. Preserve cross-links, contradictions, and provenance.
4. File valuable query outputs back into the wiki when they deserve to persist.
5. Periodically lint the vault for structural and epistemic health.

## Domain

This wiki covers seismic analysis and design, structural dynamics, earthquake engineering, design codes, modeling workflows, detailing practice, and related theory. It is intended to compound knowledge about seismic demand, capacity, ductility, response modification, nonlinear behavior, code provisions, and practical engineering judgment across analysis and design tasks.

## Conventions

- File names: lowercase, hyphens, no spaces (e.g., `response-spectrum-analysis.md`, `capacity-design.md`)
- Every wiki page starts with YAML frontmatter
- Use `[[wikilinks]]` to link between pages (minimum 2 outbound links per page)
- When updating a page, always bump the `updated` date
- Every new page must be added to `index.md` under the correct section
- Every action must be appended to `log.md`
- Raw sources in `raw/` are immutable; interpretation and synthesis belong only in wiki pages
- Prefer concise engineering summaries with assumptions, limitations, and code/jurisdiction context stated clearly
- Time-sensitive or jurisdiction-specific claims should identify the applicable code edition, standard, or publication date
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

- Domain: seismic, earthquake, structural, geotechnical, dynamics, nuclear, code, detailing
- Analysis: linear-analysis, nonlinear-analysis, modal-analysis, time-history, response-spectrum, pushover, modeling
- Response: period, damping, stiffness, mass, drift, acceleration, force, ductility, overstrength, torsion, irregularity
- Design: capacity-design, performance-based, retrofit, foundation, steel, concrete, masonry, timber
- Standards: eurocode, asce, ibc, nzc, standard, guideline
- Meta: comparison, timeline, regime, controversy, assumption, limitation, query
- Actors: person, company, institution, software

Rule: every tag on a page must appear in this taxonomy. If a new tag is needed, add it here first, then use it.

## Page Thresholds

- Create a page when an entity or concept appears in 2+ sources OR is central to one source
- Add to an existing page when a source mentions something already covered
- Do not create pages for passing mentions, routine textbook phrases, or off-domain topics
- Split a page when it exceeds ~200 lines
- Archive a page when its content is fully superseded

## Entity Pages

One page per notable entity. Include:

- Overview / what it is
- Key facts and dates
- Relevance to seismic analysis or design practice
- Relationships to other entities via [[wikilinks]]
- Source references

Examples: design standards, software packages, institutions, notable researchers, major codes.

## Concept Pages

One page per concept or topic. Include:

- Definition / explanation
- Why it matters in seismic analysis or design
- Current state of knowledge or practice
- Assumptions, limitations, and common failure modes
- Related concepts via [[wikilinks]]

Examples: response reduction factor, modal participation, accidental torsion, confinement detailing, drift limits.

## Comparison Pages

Side-by-side analyses. Include:

- What is being compared and why
- Dimensions of comparison (table preferred where useful)
- Verdict or synthesis
- Sources

Examples: response spectrum vs time-history analysis, force-based vs displacement-based design, code approaches across standards.

## Query Pages

File substantial answers worth keeping, plus open questions or contraditions to resolve. Include:

- The original question
- A concise answer
- Key supporting points
- Linked pages for follow-up
- Sources consulted
- Naming convention for query pages: answer-oriented slugs, for example `queriers/how-the-ingest-loop-works.md`.

## Update Policy

When new information conflicts with existing content:

1. Check the dates — newer standards or publications generally supersede older ones
2. If genuinely contradictory, note both positions with dates and sources
3. Mark the contradiction in frontmatter: `contradictions: [page-name]`
4. Flag for user review in the next lint report

## Domain Heuristics

- Distinguish code minimums from best-practice engineering judgment
- Separate elastic analysis assumptions from inelastic design intent
- State whether claims apply to analysis, detailing, assessment, retrofit, or code compliance
- Prefer explicit note of load path, ductility mechanism, and likely failure mode
- Treat jurisdiction-specific requirements as local unless generalized carefully
- When possible, connect design rules back to structural dynamics and physical behavior rather than rote clause citation

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
