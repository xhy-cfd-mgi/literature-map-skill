---
name: literature-map
description: Build a scholarly literature reconnaissance map for a research topic, field, method, mechanism, or paper set. Use when Codex needs to discover seminal papers, high-impact reviews, citation lineages, renamed/adjacent mechanisms, research branches, keyword/abstract/title matches, negative-search clues, legal OA full-text options, Zotero collection structures, prioritized reading lists, or a field "genealogy" before detailed paper reading.
---

# Literature Map

## Overview

Use this skill to turn a broad research interest into a structured literature reconnaissance: founders, branches, renamed adjacent mechanisms, landmark papers, current frontiers, and a prioritized reading/download plan. Favor metadata, abstracts, citation networks, and legal open-access discovery before attempting full-text retrieval.

The job is not "find some PDFs." The job is literature reconnaissance + citation tracing + field-map construction + targeted full-text acquisition.

## Four-Round Process

1. Reconnaissance.
   - Translate the user's need into seed concepts.
   - Build keyword groups for mechanisms, methods, objects/systems, outcomes, and exclusions.
   - Search title, abstract, and keyword matches separately when possible.
   - Output a keyword tree, core concepts, major clusters, key reviews, and an initial pool of about 100-300 candidates when the task scope justifies it.

2. Lineage tracing.
   - Identify "ancestor" papers by time, citations, repeated appearance in references, and cross-branch centrality.
   - Distinguish early mechanism papers from method-opening papers and application-opening papers.
   - Output a timeline, founder candidates, high-citation nodes, repeatedly cited foundations, and main technical routes.

3. Branch positioning.
   - Locate the user's specific idea inside the map.
   - Identify which branch it belongs to, which papers are closest, what has been done, what is missing, and where innovation may live.
   - Include adjacent or control branches when they clarify the user's niche.

4. Deep reading and acquisition.
   - Reduce the map to a core reading set, usually 20-50 papers.
   - Download or point to legal OA PDFs/XML first.
   - Put closed papers in a to-acquire list with DOI, access route, and priority.
   - Prepare extraction tables for detailed reading.

## Core Workflow

1. Clarify scope.
   - Restate the research question as a map target.
   - Define inclusions and exclusions: topic, organism/material/system, method class, time span, active vs passive mechanisms, application domain, and whether reviews count.
   - If scope is broad, produce v1 around 30-80 core papers rather than pretending to be exhaustive.

2. Build the keyword tree.
   - Create 4-6 keyword groups: mechanism, methods/devices, objects/systems, outcomes/metrics, comparator branches, exclusion terms.
   - Include synonyms, abbreviations, older terminology, and spelling variants.
   - Include "negative-search" terms: papers that may study the same physical mechanism without using the user's application words.
   - Search by combinations, not one linear query.

3. Seed with reviews and known nodes.
   - Find recent reviews to learn vocabulary and branches.
   - Find older/high-citation primary papers repeatedly cited by reviews.
   - Track both "method ancestors" and "application ancestors" when the field combines two domains.

4. Expand citation neighborhoods.
   - Backward snowball: references of seed reviews and seminal papers.
   - Forward snowball: citing papers of seminal papers, especially reviews and branch-opening papers.
   - Use citation count carefully: normalize by year and field; include low-citation new papers only when they clearly define an emerging branch.
   - Score candidates using total citations, citations per year, citation by core papers, repeated appearance in references, and whether they connect multiple clusters.

5. Classify papers by role.
   - Founder: early, frequently cited, defines the core method/problem.
   - Branch opener: first or representative paper for a subroute.
   - Review: synthesizes history, terminology, or application space.
   - Methods/tools: device, algorithm, dataset, assay, synthesis route, or benchmark.
   - Frontier: recent, high-quality, fast-growing, or technically relevant.
   - Negative/limitation paper: reports damage, low efficiency, cell-type dependence, failure modes, or competing explanations.
   - Context only: useful citation-network node but not a reading priority.

6. Produce the map before downloading.
   - Do not make bulk PDF downloading the goal.
   - First produce a vetted list with why each paper matters.
   - Then check legal OA availability using Unpaywall, PubMed Central, Europe PMC, arXiv/bioRxiv/medRxiv, publisher OA pages, author/institution repositories, and official project pages.
   - For closed papers, record DOI, publisher page, and access notes; do not bypass paywalls or terms.

## Search Sources

Prefer sources according to the field:

- General scholarly graph: OpenAlex, Semantic Scholar, Crossref, Google Scholar if the user can manually verify.
- Biomedical/life science: PubMed, PubMed Central, Europe PMC.
- Chemistry/materials/engineering: Crossref, OpenAlex, Semantic Scholar, publisher pages, RSC/ACS/Elsevier/Wiley metadata pages.
- Legal full text: Unpaywall, PMC OA, Europe PMC full text, arXiv/bioRxiv/medRxiv, institutional repositories, author websites.

When browsing is available, cite sources in the final answer. When exact citation counts or latest papers matter, verify live because counts and newest papers change.

## Output Contract

For a first-pass map, return:

1. Scope statement: one paragraph explaining what is included and excluded.
2. Keyword expansion table: mechanism, method, object/system, outcome, comparator, negative-search, and exclusion terms.
3. Field skeleton: a small text or Mermaid map showing main branches and relationships.
4. Timeline and lineage: early mechanisms -> method openings -> application routes -> current frontiers.
5. Seminal nodes: a table of 5-15 founder/branch-opening papers with DOI/link, year, role, and why it matters.
6. Layered reading list grouped as Level 0-5.
7. Branch summaries: 3-8 short sections covering mechanism, typical systems, key metrics, representative papers, and limitations.
8. User-branch positioning: closest papers, likely novelty space, and adjacent branches to watch.
9. OA/download plan: mark OA likely/confirmed, closed, needs institutional access, and not worth downloading yet.
10. Zotero collection/tag plan when useful.
11. Next-step proposal: identify which branch to deepen and what evidence table to build next.

Use this layered reading-list structure:

- Level 0: must-read reviews, usually 3-5 papers.
- Level 1: ancestor/founder papers, usually 3-8 papers.
- Level 2: mainstream technical route, usually 10-20 papers.
- Level 3: papers closest to the user's proposed branch, usually 10-20 papers.
- Level 4: recent hotspots, usually 10-30 papers.
- Level 5: negative evidence, limitations, failures, controversies, and mechanism-adjacent papers.

For deeper follow-up, produce structured extraction tables:

- Paper identity: title, authors, year, DOI, venue.
- Citation count or influence signal when verified.
- Branch and role.
- Abstract relevance.
- Method/device/material/system.
- Key parameters.
- Outcomes and metrics.
- Controls/comparators.
- Limitations.
- Why it matters to the user's target.
- OA/full-text status.
- PDF/Zotero status if managing a library.

See `references/output-templates.md` for compact table templates.

## Quality Rules

- Separate "important to the field" from "important to the user's question."
- Do not overtrust review narratives; use them to find primary sources.
- Prefer primary papers for claims about who introduced a method or structure.
- Flag uncertain ancestry as "candidate founder" until confirmed by multiple sources.
- Avoid citation-count monoculture: include classic low-citation technical papers if later work depends on their concept.
- Search for the same mechanism under different names; do not assume the user's wording is how the field describes it.
- Include negative and adjacent literatures when they explain mechanism or failure modes.
- Keep closed-access papers in the map when they are central, but only retrieve full text through lawful user-provided access or OA alternatives.
- Make the map iterative: v1 is a hypothesis, then refine after user feedback and deeper citation tracing.

## References

- Read `references/search-strategy.md` when designing queries or expanding a field.
- Read `references/output-templates.md` when creating tables or a final map artifact.
