---
title: "LLM-Maintained Knowledge Wikis"
type: concept
tags: [knowledge-management, llms, wikis, synthesis, secondbrain]
sources: [llm-wiki.md]
created: 2026-07-26
updated: 2026-07-26
status: developing
---

# LLM-Maintained Knowledge Wikis

An LLM-maintained knowledge wiki is a personal or team knowledge system where the LLM does not merely retrieve raw documents at query time. Instead, it incrementally builds and maintains a persistent set of structured, interlinked Markdown pages. The wiki becomes a compounding artifact: each source is integrated once, cross-referenced, and kept current as new material arrives.

The core pattern differs from [[retrieval-augmented-generation]] because the synthesis is stored. In a typical RAG workflow, the model repeatedly rediscovers relevant chunks from source documents whenever a question is asked. In an LLM-maintained wiki, the model has already extracted the important claims, updated relevant pages, connected related concepts, and flagged contradictions. Later queries operate against this maintained intermediate layer instead of raw source fragments alone.

The human's role is to curate inputs, direct the investigation, ask good questions, and review the resulting knowledge. The LLM's role is the maintenance labor: summarizing, filing, linking, revising, logging, and keeping the wiki internally coherent. This turns knowledge management from a manual bookkeeping burden into an agent-maintained workflow.

The pattern fits domains where knowledge accumulates over time: personal development, health notes, research projects, course notes, book companion wikis, competitive analysis, due diligence, trip planning, and internal team knowledge bases. It is especially useful when later questions require synthesis across many prior sources.

## Architecture

The system has three main layers:

- Raw sources are the immutable source of truth: articles, notes, papers, transcripts, images, or other captured material.
- The wiki is the LLM-owned synthesis layer: concept pages, entity pages, source summaries, comparisons, overviews, and indexes.
- The schema or agent manual defines the rules: page formats, workflows, linking conventions, ingest steps, query behavior, linting, and maintenance constraints.

This vault implements the same pattern through [[getting-started]], [[wiki-maintenance-workflows]], [[persistent-synthesis]], and an Obsidian-based Markdown graph.

## Related

- [[persistent-synthesis]]
- [[retrieval-augmented-generation]]
- [[wiki-maintenance-workflows]]
- [[obsidian]]
- [[source-llm-wiki]]
