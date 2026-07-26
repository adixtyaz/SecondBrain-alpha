# SecondBrain

SecondBrain is a git-tracked Obsidian vault maintained by an AI agent. It is designed to turn raw captures into a persistent, interlinked knowledge graph instead of repeatedly re-summarizing the same documents from scratch.

The core idea is simple: the human captures sources and asks questions; the agent reads, synthesizes, links, archives, and logs. Over time, the wiki becomes a compounding artifact.

## Current Status

This vault has been bootstrapped and has completed its first ingest.

The current wiki includes source summaries and topic pages for:

- LLM-maintained wiki systems

Start with [`wiki/overview.md`](wiki/overview.md) for the high-level synthesis, then use [`wiki/index.md`](wiki/index.md) as the catalog.

## Architecture

The vault has three main layers.

### `raw/`

The inbox. This is where new captures go before processing.

Examples:

- Notes
- Clipped articles
- PDFs
- Voice transcripts
- Markdown exports
- Images and local assets

During normal operation, the agent treats `raw/` as read-only. After successful processing, files are moved to `archive/`.

### `wiki/`

The synthesized knowledge graph. This is the primary product of the system.

The agent creates and maintains pages here, including:

- Concept pages
- Entity pages
- Source summaries
- Index and overview pages

Every wiki page should have YAML frontmatter and should link to related pages using Obsidian wikilinks.

### `archive/`

The permanent historical record. Once a source has been processed, the original file is moved here and must not be modified.

This keeps the vault auditable: the wiki contains synthesized knowledge, while `archive/` preserves the source trail.

## System Files

The root files define how the system should be operated.

| File | Purpose |
| --- | --- |
| [`AGENT.md`](AGENT.md) | Operating manual for the AI agent. Read this at the start of every work session. |
| [`RULES.md`](RULES.md) | Non-negotiable vault rules, including immutability, wiki integrity, linking, logging, formatting, and safety constraints. |
| [`LOG.md`](LOG.md) | Append-only chronological record of meaningful operations. |
| [`README.md`](README.md) | Human-facing repository guide. |

## How To Use This Vault

### 1. Capture

Drop new material into `raw/`.

Do not worry about organizing it first. The system is designed for low-friction capture.

Good raw inputs include:

- Article clips
- Personal notes
- Research documents
- Book notes
- Transcripts
- Reports
- PDFs

### 2. Ingest

Ask the agent:

```text
Process raw
```

or:

```text
Ingest
```

The agent should:

1. Read `AGENT.md` and `RULES.md`.
2. Scan `raw/`.
3. Read each source.
4. Identify topics and entities.
5. Create or update relevant wiki pages.
6. Create source summary pages when useful.
7. Update `wiki/index.md`.
8. Update `wiki/overview.md` when the overall synthesis changes.
9. Move processed files into `archive/`.
10. Append the operation to `LOG.md`.

### 3. Query

Ask questions about the wiki.

The agent should read `wiki/index.md` first, then read the relevant pages in full before answering. Answers should cite wiki pages using Obsidian-style references such as `[[ai-2027-scenario]]`.

### 4. Lint

Ask:

```text
Lint the wiki
```

The agent should check for:

- Orphan pages
- Stub pages
- Broken wikilinks
- Stale pages
- Missing concept pages
- Overview drift
- Contradictions or unresolved uncertainty

The lint report should be appended to `LOG.md`.

## Page Types

Wiki pages use the schema defined in `AGENT.md`.

Common page types:

- `concept`: an idea, framework, principle, or topic
- `entity`: a person, organization, book, tool, or place
- `source`: a summary of one specific source document
- `index`: reserved for `wiki/index.md`
- `overview`: reserved for `wiki/overview.md`

Status values:

- `stub`: placeholder or incomplete page
- `developing`: useful but still growing
- `mature`: well-supported and stable
- `needs-review`: possibly stale, contradicted, or uncertain

## Operating Principles

This repo is meant to be maintained conservatively.

- Never delete source material.
- Never edit archived sources.
- Never overwrite a wiki page without reading it first.
- Prefer merging and extending over replacing.
- Keep one clear topic per wiki page.
- Add links between related pages.
- Flag uncertainty instead of hiding it.
- Log meaningful operations.
- Treat the wiki as a living artifact, not a static notes folder.

## Git Workflow

This vault is a git repository. Commits act as checkpoints in the evolution of the knowledge base.

Natural commit points include:

- After bootstrapping the vault
- After an ingest
- After a lint pass
- After major structural edits
- After updating operating rules or documentation

Suggested commit style:

```text
ingest: process new raw sources
lint: add wiki health report
docs: add repository README
update: revise overview after ingest
```

## Privacy

This repository is intended to remain private unless the owner explicitly decides otherwise. The vault may contain personal notes, research trails, and archived source material.

Before sharing the repo, review:

- `raw/`
- `archive/`
- `wiki/`
- `LOG.md`
- Obsidian workspace state in `.obsidian/`

## Repository Map

```text
SecondBrain/
  AGENT.md
  RULES.md
  LOG.md
  README.md
  raw/
    .gitkeep
    assets/
  wiki/
    index.md
    overview.md
    getting-started.md
    ...
  archive/
    .gitkeep
    ...
  .obsidian/
```

## First Files To Read

For a human:

1. [`README.md`](README.md)
2. [`wiki/overview.md`](wiki/overview.md)
3. [`wiki/index.md`](wiki/index.md)
4. [`AGENT.md`](AGENT.md)
5. [`RULES.md`](RULES.md)

For an AI agent:

1. [`AGENT.md`](AGENT.md)
2. [`RULES.md`](RULES.md)
3. [`wiki/index.md`](wiki/index.md)
4. [`wiki/overview.md`](wiki/overview.md)
5. [`LOG.md`](LOG.md)

## Maintenance Notes

The wiki should improve with every ingest. If a new source does not produce better pages, stronger links, clearer uncertainty, or a better overview, the ingest probably did not go deep enough.

The goal is not to collect documents. The goal is to build an increasingly useful map of what the user is learning, investigating, and trying to understand.
