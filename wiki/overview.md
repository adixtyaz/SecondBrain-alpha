---
title: "Wiki Overview"
type: overview
tags: [overview, synthesis, wiki]
sources: [llm-wiki.md]
created: 2026-07-03
updated: 2026-07-26
status: developing
---

# Overview

This page is a high-level synthesis of everything currently in the wiki. The agent keeps it current as new sources are ingested. It is the best starting point for understanding what this knowledge base contains.

---

## Current State

The wiki currently centers on one foundational pattern: using LLMs to maintain a persistent, interlinked knowledge wiki rather than relying only on query-time document retrieval.

The first ingested source, [[source-llm-wiki]], argues that a useful SecondBrain should have three layers: immutable raw sources, an LLM-maintained wiki, and a schema or operating manual that defines the workflows. This vault follows that structure directly through `/raw`, `/wiki`, `/archive`, `AGENT.md`, and `RULES.md`.

---

## Active Themes

- [[llm-maintained-knowledge-wikis]] - the overall pattern for turning captured sources into a maintained Markdown knowledge graph.
- [[persistent-synthesis]] - the principle that useful summaries, comparisons, contradictions, and insights should be saved as durable wiki knowledge.
- [[wiki-maintenance-workflows]] - the recurring ingest, query, and lint operations that keep the wiki useful.
- [[retrieval-augmented-generation]] - the contrasting pattern where knowledge is retrieved and reconstructed at query time.
- [[obsidian]] - the local interface for reading, linking, and navigating the graph.

---

## Knowledge Gaps

- The current wiki has only one external source, so all topic pages are developing rather than mature.
- Future sources could deepen the practical side of this system: vault schemas, Obsidian workflows, agent evaluation, personal knowledge management, and examples of mature LLM-maintained wikis.
- The source contains abstract guidance rather than empirical evidence, so claims about effectiveness should be refined as the vault accumulates real usage and additional sources.

---

## Last Updated

This overview was last revised during: `ingest | llm-wiki.md`
