---
title: "Retrieval-Augmented Generation"
type: concept
tags: [rag, llms, retrieval, knowledge-management, ai]
sources: [llm-wiki.md]
created: 2026-07-26
updated: 2026-07-26
status: developing
---

# Retrieval-Augmented Generation

Retrieval-augmented generation, or RAG, is a common pattern where an LLM answers questions by retrieving relevant chunks from a collection of source documents at query time. The source note uses NotebookLM, ChatGPT file uploads, and many RAG systems as examples of this broad interaction style.

RAG is useful because it gives the model access to external documents without requiring the model to memorize them. Its limitation, in the source's framing, is that knowledge is reassembled repeatedly. Each subtle question may require the system to find and combine fragments again, even if a previous answer already produced a useful synthesis.

[[llm-maintained-knowledge-wikis]] address that limitation by storing the synthesized layer. The raw documents remain the source of truth, but the wiki becomes a maintained map of what has already been understood.

## Related

- [[llm-maintained-knowledge-wikis]]
- [[persistent-synthesis]]
