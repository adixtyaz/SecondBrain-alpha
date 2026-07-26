# RULES.md
# The Non-Negotiable Law of This SecondBrain

Every rule in this file applies in every session, every operation, without exception.
If a rule conflicts with a user instruction, follow the rule and note the conflict in LOG.md.

---

## IMMUTABILITY RULES

R1. Never delete any file from /raw, /wiki, or /archive. Move only, never delete.
R2. Never modify a file after it has been moved to /archive. It is a permanent record.
R3. Treat /raw as read-only during all wiki operations. Never write or edit files there.
R4. When processing files from /raw, move them to /archive after successful wiki integration, preserving the original filename. If a filename collision exists in /archive, append _YYYYMMDD before the extension.

## WIKI INTEGRITY RULES

R5. Before updating any wiki page, read its current content in full. Never overwrite blindly. Merge, extend, or revise - never erase prior knowledge unless it is factually wrong and a newer source proves it.
R6. One topic per wiki file. If a raw source covers multiple distinct topics, create or update multiple wiki pages accordingly.
R7. All wiki filenames must use kebab-case. Examples: machine-learning.md, naval-ravikant.md, sleep-optimization.md. No spaces, no capitals, no underscores.
R8. Every wiki page must include a YAML frontmatter block at the top (see AGENT.md for the required schema).
R9. When you are uncertain whether information is accurate, note it inline with a [?] marker and log the uncertainty. Never fabricate or assume.
R10. Never create a wiki page for something you cannot support with at least one source from /raw or /archive.
R11. When a raw source contradicts an existing wiki page, do not silently overwrite. Note the contradiction explicitly in the wiki page under a ## Contradictions or ## Open Questions section, and log it.
R12. After ingesting any source, update wiki/index.md and evaluate whether wiki/overview.md needs revision.

## LINKING RULES

R13. Use relative Obsidian wikilinks for all internal references: [[page-name]] or [[page-name|Display Text]].
R14. When creating or updating a wiki page, actively look for related existing pages and add wikilinks to them. Orphan pages are failures.
R15. Never use absolute paths or external URLs as internal links.

## LOG RULES

R16. Every meaningful operation must be logged in LOG.md immediately after it completes.
R17. Log entries must start with a consistent prefix: ## [YYYY-MM-DD] operation | description
R18. Valid operation types: ingest, update, create, merge, move, error, lint, query, init.
R19. Never delete or edit past log entries. LOG.md is append-only.

## FORMATTING RULES

R20. Default voice: clear, factual, direct. No motivational filler. No hedging without cause.
R21. Use headings only when a page is long enough to need navigation (roughly 300+ words).
R22. Use bullet points only for genuinely enumerable content, not as a default writing mode.
R23. Preserve the user's own phrasing when it appears in raw notes and carries signal - do not neutralize everything into generic encyclopedia tone.
R24. Do not add emojis to wiki content unless the source explicitly contained them and they carry meaning.

## SAFETY RULES

R25. Do not make any external network calls unless the user explicitly requests a web search.
R26. Do not touch any file outside the vault directory you have been given access to.
R27. Do not modify RULES.md, AGENT.md, or LOG.md structure - only append to LOG.md.
R28. If you encounter a file type you cannot read (e.g., a binary PDF), log it as skipped with the reason and move it to /archive anyway so it is not re-processed.
