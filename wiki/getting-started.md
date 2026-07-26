---
title: "Getting Started with This SecondBrain"
type: concept
tags: [meta, system, how-to]
sources: []
created: 2026-07-03
updated: 2026-07-03
status: mature
---

# Getting Started with This SecondBrain

This vault operates as a compounding knowledge system. The AI agent synthesizes raw captures into an interlinked wiki that gets richer over time.

## How to Use It

**Step 1 - Capture.** Drop anything into `/raw`. Notes, PDFs, voice transcripts, clipped articles, images. Don't organize. Don't rename. Just drop.

**Step 2 - Ingest.** Tell the agent to process `/raw`. It reads every file, synthesizes the key information into wiki pages, links related entries, and moves processed files to `/archive`.

**Step 3 - Read.** Browse `/wiki` in Obsidian. Use the graph view to see connections. Ask the agent questions - it reads the wiki and synthesizes answers with citations.

**Step 4 - Lint (periodically).** Tell the agent to run a health check. It finds orphan pages, stale content, missing links, and coverage gaps.

## What the Agent Does

- Creates and updates pages in [[wiki/index|wiki/index]] and [[wiki/overview|wiki/overview]]
- Links related concepts using Obsidian wikilinks
- Flags contradictions rather than silently overwriting
- Moves processed raw files to `/archive` - nothing is ever deleted
- Logs every action in [[LOG]]

## What the Agent Does Not Do

- Browse the web (unless you explicitly ask)
- Delete files
- Edit files in `/raw` or `/archive`
- Guess when uncertain - it flags and logs instead

## Key Files

| File | Purpose |
|------|---------|
| `AGENT.md` | Agent's full operating manual |
| `RULES.md` | Non-negotiable rules for every operation |
| `LOG.md` | Append-only action log |
| `wiki/index.md` | Catalog of all wiki pages |
| `wiki/overview.md` | High-level synthesis of the full wiki |

## Related

*No related pages yet - this is the first page.*
