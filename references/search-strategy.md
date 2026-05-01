# Search Strategy

## Query Pattern

Create grouped query blocks:

```text
mechanism:
  "<physical/biological mechanism>"
  "<synonym>"
  "<older term>"
  "<renamed or adjacent mechanism>"

method/device/approach:
  "<method phrase>"
  "<abbreviation>"
  "<specific structure/tool>"

object/system:
  "<cell/material/model/system>"
  "<clinically relevant object>"
  "<benchmark object>"

outcome/metric:
  "<metric>"
  "<mechanism>"
  "<performance term>"

comparator/control branch:
  "<competing method>"
  "<standard baseline>"
  "<adjacent technology>"

negative-search:
  "<damage/failure mechanism>"
  "<injury/stress term>"
  "<same mechanism without target application>"

filters/exclusions:
  review
  "seminal"
  "first"
  -"unwanted topic"
```

Run combinations such as:

```text
"mechanism" "method phrase" review
"specific structure" "mechanism"
"object/system" "outcome metric" "method phrase"
"negative-search term" "object/system"
"founder paper title" citing papers review
```

## Negative Search

Use negative search when the user's idea may be described under different language or in a non-application field.

Examples:

- A delivery idea may appear in literature as membrane damage, rupture, repair, stress, deformation, or viability loss rather than "transfection."
- A device idea may appear as flow focusing, constriction, impingement, shear, collision, squeezing, hydroporation, or deformation rather than the user's exact geometry.
- A biological mechanism may appear in pathology, biomechanics, hemolysis, leukocyte deformation, microcirculation, or cell-injury literature before being used as a delivery method.

Search for both enabling papers and warning papers. Warning papers are useful for identifying failure modes and novelty gaps.

## Citation Snowballing

Use reviews to identify names and branches, then verify with primary papers.

Backward snowball:

- Extract references from S/A papers and reviews.
- Look for repeated early citations.
- Identify method papers that predate application papers.

Forward snowball:

- Inspect citing papers of founder nodes.
- Prioritize later reviews, comparisons, and papers that introduce new structures or applications.
- Track whether citations form distinct branches or merely reuse a method.

## Ranking Signals

Use multiple signals together:

- Title/abstract/keyword match to the user's scope.
- Citation count and citation velocity.
- Citations by the current core paper set.
- Repeated appearance in references of independent reviews.
- Venue relevance and field prestige.
- Review recurrence: appears in several independent reviews.
- Method centrality: supplies a device, protocol, theory, dataset, or metric.
- Branch coverage: connects otherwise separate clusters.
- Practical relevance: gives parameters, comparators, or reproducible details.
- Negative value: explains limitations, damage, low efficiency, toxicity, or why a route failed.

## Legal Full-Text Order

1. Unpaywall OA URL by DOI.
2. PMC / Europe PMC full text for biomedical fields.
3. arXiv, bioRxiv, medRxiv, ChemRxiv, institutional repositories.
4. Publisher OA page.
5. Author lab page or project page.
6. User-provided institutional access.
7. Zotero Connector/manual saving for closed papers before full-text retrieval.

Do not use browser automation to bypass publisher access controls. Do not present a closed publisher PDF as downloadable unless it is legally available to the user.
