---
title: "Source: LLM Wiki"
type: source
tags: [source, llms, wikis, knowledge-management, obsidian]
sources: [llm-wiki.md]
created: 2026-07-26
updated: 2026-07-26
status: mature
---

# Source: LLM Wiki

`llm-wiki.md` is an idea note describing a pattern for building personal or team knowledge bases with LLM agents. Its main claim is that LLMs should not only retrieve from documents at query time; they should maintain a persistent wiki that accumulates synthesis over time.

The note contrasts this with [[retrieval-augmented-generation]]. RAG retrieves relevant chunks for each query, while an [[llm-maintained-knowledge-wikis|LLM-maintained wiki]] stores the synthesis as Markdown pages: summaries, concept pages, entity pages, indexes, overviews, contradictions, and cross-references.

The proposed architecture has three layers: immutable raw sources, an LLM-owned wiki, and a schema or agent manual that defines the operating rules. The note describes ingest, query, and lint as the core workflows. Ingest integrates new sources into the wiki. Query synthesizes answers from the maintained wiki and can file valuable answers back into it. Lint checks for contradictions, stale pages, orphans, missing cross-references, and knowledge gaps.

The source emphasizes that the human remains responsible for curation, direction, and judgment. The LLM handles the maintenance burden that normally causes wikis to decay: bookkeeping, cross-referencing, updating pages, logging changes, and keeping the graph coherent.

## Key Takeaways

- The wiki is a persistent, compounding artifact, not just a retrieval index.
- Raw sources remain the source of truth; the wiki is the maintained synthesis layer.
- Good answers from queries should be preserved when they add durable value.
- Linting is essential because an agent-maintained wiki still needs health checks.
- Obsidian works well as the browsing and graph interface for this pattern.

## Related

- [[llm-maintained-knowledge-wikis]]
- [[persistent-synthesis]]
- [[wiki-maintenance-workflows]]
- [[obsidian]]
