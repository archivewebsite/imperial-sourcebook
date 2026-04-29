# Imperial Sourcebook Agent Rules

These rules apply to any agent editing files under `D:\Imperial Sourcebook`.

## Required Reads

- Read `CHANGELOG.md`, `PATH.md`, and `README.md` before making structural or routing decisions.
- Read the nearest folder `README.md` before creating new buckets or moving notes in that area.

## Changelog Requirement

- If you are the top-level or orchestrating agent and you keep any file edit under this vault, update `CHANGELOG.md` in the same task before finishing.
- Merge into the existing `## YYYY-MM-DD` heading for today when it already exists.
- Small note-level edits may use short bullets. Larger reorganizations should use fuller sections.
- If a run stops early but leaves kept changes in place, log the partial state explicitly in `Notes` instead of skipping the changelog.
- Skip the changelog only for dry-runs, previews, planning-only work, delegated worker-only work, or verified no-op runs.
- Delegated workers do not edit `CHANGELOG.md`; they return a changelog-ready handoff summary to the parent.

## Edit Discipline

- Keep folder roles aligned with `PATH.md`, `README.md`, and folder-level `README.md` files.
- Do not create new top-level buckets unless the task clearly requires it.
- When routing notes, prefer the existing documented buckets over inventing new ones.

## Naming Convention

- Use title-case English note titles, sentence-case Indonesian note titles, and normal acronym casing such as `UTBK` or `AI`.
- Do not leave note titles or filenames in ALL-CAPS unless the whole title is an acronym.
- Avoid leading articles such as `The`, `A`, and `An` when the title still reads naturally without them.
- Final filed notes must not keep `(Inbox YYYY-MM-DD)` suffixes. Use a clearer topic title, a descriptive variant, or wikilink display text when a duplicate needs context.
- Keep filenames readable, concise, and filesystem-safe. Prefer letters, numbers, spaces, and hyphens.

## Note Type Taxonomy

Use these note types as plain-language routing and lifecycle guidance. Do not add vault-wide metadata fields or templates unless the user explicitly asks for them.

- `Concept`: a durable explanation of one idea, model, term, or principle.
- `Clipping`: imported or source-close material that still needs cleanup, extraction, or routing.
- `Soal`: an unsolved or prompt-like practice question.
- `Worked Example`: a solved problem, answer breakdown, or reasoning trace.
- `MOC`: a map-of-content note that links and orients a topic cluster.
- `Stub`: a note below the useful-content threshold; it needs expansion or routing.
- `Vocabulary Row`: one translated word or phrase inside a language vocabulary table.
- `Cheatsheet`: compact reference material meant for quick lookup.

## Stub Policy

- A usable note needs at least a clear title plus a scope sentence or one-paragraph summary.
- Notes below that threshold are stubs.
- Stubs belong only in `Inbox/` or `Curiosity Shelf/` unless a folder README explicitly allows them.
- When expanding a stub, add enough context that a future reader can understand why the note exists.

## Dedup Policy

- Detect likely duplicates with case-insensitive and punctuation-insensitive title comparisons, then confirm by reading the notes.
- Keep the most developed note as the primary record.
- Fold unique material from the weaker duplicate into the primary note as an appendix or clearly labeled retained context when a merge is requested.
- Preserve inbound link safety by leaving clear wikilink display text or a redirect note when removing or renaming an old title would break existing references.
- Do not delete an unreviewed duplicate only because the title looks similar.

## Wikilink Discipline

- Use bare note-name wikilinks such as `[[Note Name]]`, not path-based links, when linking notes.
- Use wikilink display text such as `[[Note Name|variant text]]` for alternate phrasing, translations, or old titles.
- Use embeds only for canvases, shared tables, or material that genuinely needs to render inside another note.
- Use block links only for direct citation or exact reusable passages.

## Tag Policy

- Use `TAGS.md` as the canonical tag registry.
- New tag roots or new recurring tags must be added to `TAGS.md` before they are used broadly.
- Do not backfill tags across existing notes unless the user asks for a dedicated tagging pass.

## Attachment Policy

- Store supporting files under `Attachments/`.
- Prefer `YYYYMMDD-slug.ext` for newly named assets, or a short descriptive filename when the date is not useful.
- Keep meaning in markdown notes. Attachments should support notes, not replace them.
- Concept-note images should have useful alt text when embedded.
- Do not create attachment-only knowledge records.

## Move And Rename Policy

- Use Obsidian rename or a link-aware workflow when renaming or moving notes so internal links stay intact.
- Do not use raw operating-system renames for content notes unless you also verify and update affected links.
- Cross-folder moves must keep the destination aligned with `PATH.md`, the root `README.md`, and the nearest folder `README.md`.
- If a move changes folder meaning or creates a new recurring pattern, update the affected folder README and this changelog in the same task.
