---
title: "Wiki Maintenance Workflows"
type: concept
tags: [workflow, knowledge-management, llms, obsidian, maintenance]
sources: [llm-wiki.md]
created: 2026-07-26
updated: 2026-07-26
status: developing
---

# Wiki Maintenance Workflows

Wiki maintenance workflows are the repeatable operations that keep an LLM-maintained wiki useful over time. The source identifies three core workflows: ingest, query, and lint.

Ingest begins when a human adds a source to the raw collection and asks the LLM to process it. The LLM reads the source, creates or updates relevant concept and entity pages, writes a source summary when useful, updates the index, and logs the operation. A single source can touch many pages because the goal is integration, not isolated summarization.

Query uses the wiki as the first layer of context. The LLM reads the index, opens relevant pages, and synthesizes an answer with citations to the wiki. Strong query answers can become wiki material themselves, turning good conversations into persistent knowledge.

Lint is the health-check workflow. The LLM periodically looks for contradictions, stale claims, orphan pages, missing cross-references, important concepts without pages, and gaps that may need new sources. Linting is what prevents a wiki from slowly becoming inconsistent as it grows.

These workflows make [[llm-maintained-knowledge-wikis]] practical. The LLM is valuable not only because it can summarize, but because it can perform the recurring maintenance work that humans usually abandon.

## Related

- [[llm-maintained-knowledge-wikis]]
- [[persistent-synthesis]]
- [[obsidian]]
