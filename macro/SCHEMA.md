# Wiki Schema

## Domain
This wiki covers Bitcoin, macroeconomics, liquidity, market structure, and cycle theory. It is intended to compound knowledge about Bitcoin market cycles, monetary conditions, macro regime shifts, on-chain context, sentiment, valuation frameworks, and related people, institutions, and narratives.

## Conventions
- File names: lowercase, hyphens, no spaces (e.g., `global-liquidity.md`, `bitcoin-four-year-cycle.md`)
- Every wiki page starts with YAML frontmatter
- Use `[[wikilinks]]` to link between pages (minimum 2 outbound links per page)
- When updating a page, always bump the `updated` date
- Every new page must be added to `index.md` under the correct section
- Every action must be appended to `log.md`
- Raw sources in `raw/` are immutable; analysis belongs only in wiki pages
- Prefer concise, synthesis-first writing with explicit notes on disagreement, uncertainty, and time-sensitivity
- Time-sensitive claims should include dates or period labels

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
- Assets: bitcoin, crypto, commodities, equities, bonds, dollar
- Macro: macro, liquidity, inflation, rates, credit, recession, growth, policy, fiscal, monetary
- Cycles: cycle, halving, business-cycle, debt-cycle, liquidity-cycle, election-cycle, market-structure
- Analysis: valuation, onchain, sentiment, positioning, flows, volatility, risk, thesis
- Actors: person, company, institution, government, central-bank
- Meta: comparison, timeline, regime, narrative, controversy, prediction, query

Rule: every tag on a page must appear in this taxonomy. If a new tag is needed, add it here first, then use it.

## Page Thresholds
- Create a page when an entity or concept appears in 2+ sources OR is central to one source
- Add to an existing page when a source mentions something already covered
- Do not create pages for passing mentions, generic market chatter, or off-domain topics
- Split a page when it exceeds ~200 lines
- Archive a page when its content is fully superseded

## Entity Pages
One page per notable entity. Include:
- Overview / what it is
- Key facts and dates
- Role in Bitcoin, macro, or cycle-theory context
- Relationships to other entities via [[wikilinks]]
- Source references

Examples: people, central banks, companies, ETFs, research firms, nations, protocols.

## Concept Pages
One page per concept or topic. Include:
- Definition / explanation
- Why it matters for Bitcoin, macro, or cycles
- Current state of knowledge
- Open questions, debates, or failure modes
- Related concepts via [[wikilinks]]

Examples: global liquidity, halving reflexivity, M2, sovereign debt cycles, real yields, dollar liquidity.

## Comparison Pages
Side-by-side analyses. Include:
- What is being compared and why
- Dimensions of comparison (table preferred where useful)
- Verdict or synthesis
- Sources

Examples: Bitcoin vs gold, hard landing vs soft landing, halving theory vs liquidity theory.

## Query Pages
File substantial answers worth keeping. Include:
- The original question
- A concise answer
- Key supporting points
- Linked pages for follow-up
- Sources consulted

## Update Policy
When new information conflicts with existing content:
1. Check the dates — newer sources generally supersede older ones
2. If genuinely contradictory, note both positions with dates and sources
3. Mark the contradiction in frontmatter: `contradictions: [page-name]`
4. Flag for user review in the next lint report

## Domain Heuristics
- Prefer multi-factor explanations over single-cause market narratives
- Separate structural drivers from short-term catalysts
- Distinguish descriptive claims, explanatory claims, and predictions
- Note when a thesis is cyclical, secular, reflexive, or regime-dependent
- Treat macro and market commentary as time-sensitive unless clearly timeless
- When possible, connect Bitcoin claims to macro liquidity, policy, market structure, and positioning rather than isolated folklore
