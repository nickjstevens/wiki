# Wiki Schema

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

## Frontmatter
```yaml
---
title: Page Title
created: YYYY-MM-DD
updated: YYYY-MM-DD
type: entity | concept | comparison | query | summary
tags: [from taxonomy below]
sources: [raw/papers/source-name.pdf]
---
```

## Tag Taxonomy
- Domain: seismic, earthquake, structural, geotechnical, dynamics, code, detailing
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
File substantial answers worth keeping. Include:
- The original question
- A concise answer
- Key supporting points
- Linked pages for follow-up
- Sources consulted

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
