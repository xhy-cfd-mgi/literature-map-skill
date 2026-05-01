# literature-map-skill

Codex skill for literature reconnaissance, citation tracing, field mapping, and targeted full-text acquisition.

## What This Skill Does

This skill helps Codex turn a broad research idea into a structured literature map. It is designed for tasks such as:

- Finding seminal papers and "ancestor" articles
- Expanding keywords across mechanisms, methods, systems, outcomes, and negative-search terms
- Building citation lineages and research branches
- Separating reviews, founder papers, mainstream routes, user-specific branches, recent hotspots, and limitations
- Checking legal open-access full-text options before closed-source papers
- Designing Zotero collections and prioritized reading lists

It is not a bulk PDF downloader. The intended workflow is:

```text
Reconnaissance -> Lineage tracing -> Branch positioning -> Deep reading and acquisition
```

## Install

Clone this repository or download it as a ZIP, then place the folder in your Codex skills directory:

```text
C:\Users\<your-user-name>\.codex\skills\literature-map
```

The folder should contain:

```text
literature-map
├── SKILL.md
├── agents
│   └── openai.yaml
└── references
    ├── output-templates.md
    └── search-strategy.md
```

Restart or refresh Codex after installing if the skill does not appear immediately.

## Usage

You can invoke it explicitly:

```text
Use $literature-map to build a literature map for microfluidic mechanoporation and carrier-free intracellular delivery.
```

Or describe the task naturally:

```text
Help me find the founder papers, main branches, recent hotspots, and OA papers for microreactors in micro chemical engineering.
```

## Example Outputs

The skill guides Codex to produce:

- Keyword expansion table
- Field skeleton or Mermaid map
- Timeline and lineage
- Seminal paper table
- Level 0-5 reading list
- Branch summaries
- User-branch positioning
- OA/download plan
- Zotero collection structure

## License

MIT License.
