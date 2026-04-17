# Wiki Schema

## Domain
This wiki covers asset management, portfolio construction, market regimes, investment process, manager research, risk management, performance attribution, and allocator decision-making. It is intended to compound knowledge about public and private markets, strategic and tactical asset allocation, manager selection, portfolio monitoring, client/investment-committee communication, and the theories and frameworks used in professional asset management.

## Conventions
- File names: lowercase, hyphens, no spaces (e.g., `portfolio-construction.md`, `factor-investing.md`)
- Every wiki page starts with YAML frontmatter
- Use `[[wikilinks]]` to link between pages (minimum 2 outbound links per page)
- When updating a page, always bump the `updated` date
- Every new page must be added to `index.md` under the correct section
- Every action must be appended to `log.md`
- Raw sources in `raw/` are immutable; synthesis and interpretation belong only in wiki pages
- Prefer concise, decision-oriented writing that distinguishes fact, framework, and opinion
- Time-sensitive claims should include dates, regime context, benchmark context, or market period labels where relevant

## Frontmatter
```yaml
---
title: Page Title
created: YYYY-MM-DD
updated: YYYY-MM-DD
type: entity | concept | comparison | query | summary
tags: [from taxonomy below]
sources: [raw/articles/source-name.md]
---
```

## Tag Taxonomy
- Asset-Classes: equities, fixed-income, credit, private-markets, real-estate, infrastructure, commodities, cash, alternatives
- Portfolio: asset-allocation, diversification, rebalancing, benchmark, liquidity, duration, leverage, hedging
- Investment-Style: active, passive, factor, value, growth, quality, momentum, income, macro, multi-asset
- Process: due-diligence, manager-selection, underwriting, monitoring, attribution, reporting, governance, thesis
- Risk: volatility, drawdown, correlation, tail-risk, concentration, scenario-analysis, stress-testing
- Actors: person, company, institution, fund, allocator, consultant
- Meta: comparison, timeline, regime, narrative, controversy, prediction, query

Rule: every tag on a page must appear in this taxonomy. If a new tag is needed, add it here first, then use it.

## Page Thresholds
- Create a page when an entity or concept appears in 2+ sources OR is central to one source
- Add to an existing page when a source mentions something already covered
- Do not create pages for passing mentions, generic market commentary, or off-domain topics
- Split a page when it exceeds ~200 lines
- Archive a page when its content is fully superseded

## Entity Pages
One page per notable entity. Include:
- Overview / what it is
- Key facts and dates
- Role in asset management practice or market structure
- Relationships to other entities via [[wikilinks]]
- Source references

Examples: fund managers, asset owners, consultants, custodians, ETF issuers, notable funds.

## Concept Pages
One page per concept or topic. Include:
- Definition / explanation
- Why it matters for portfolio construction or asset-management practice
- Current state of knowledge or common practice
- Key trade-offs, limitations, and failure modes
- Related concepts via [[wikilinks]]

Examples: strategic asset allocation, active share, tracking error, fee budgets, liquidity buckets, factor crowding.

## Comparison Pages
Side-by-side analyses. Include:
- What is being compared and why
- Dimensions of comparison (table preferred where useful)
- Verdict or synthesis
- Sources

Examples: active vs passive, strategic vs tactical allocation, internal vs external management, public vs private market exposures.

## Query Pages
File substantial answers worth keeping. Include:
- The original question
- A concise answer
- Key supporting points
- Linked pages for follow-up
- Sources consulted

## Update Policy
When new information conflicts with existing content:
1. Check the dates — newer disclosures or better evidence generally supersede older information
2. If genuinely contradictory, note both positions with dates and sources
3. Mark the contradiction in frontmatter: `contradictions: [page-name]`
4. Flag for user review in the next lint report

## Domain Heuristics
- Distinguish strategic policy decisions from tactical positioning
- Separate framework-level guidance from market-timing narratives
- Note whether claims apply to allocators, managers, advisers, or end investors
- Prefer explicit treatment of incentives, fees, liquidity, and benchmark effects
- Treat performance claims as incomplete without horizon, benchmark, and risk context
- When possible, connect investment views back to portfolio objectives, constraints, and implementation reality rather than isolated return stories
