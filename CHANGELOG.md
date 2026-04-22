# Changelog

All completed agent-driven changes to Imperial Sourcebook should be documented here.

This changelog is the required ledger for AI and agent work in this vault. Large reorganizations can use fuller entries; small note-level edits can use short bullets under the current date. Manual edits outside agent workflows can be logged too, but the rules below are enforced for agent-driven work.

## Recent Entries

Add new dated entries at the top of this section.

## 2026-04-22

### Changed
- Task type: `vault-bootstrap`
- Connected the local `D:\Imperial Sourcebook` vault to the GitHub repository `https://github.com/archivewebsite/imperial-sourcebook.git`.
- Replaced the legacy root `README.md` from the old `Resources` folder with Sourcebook-specific root documentation.
- Added `PATH.md`, `CHANGELOG.md`, `.gitignore`, and the remote `LICENSE` so the vault has the same root governance pattern as `Imperial Records`.
- Task type: `sourcebook-organization`
- Consolidated the small-bucket layout by moving `Random Questions` under `Notes`, moving `Tips and Trick` under `Personal Advice`, and relocating `Idea Backlog` to `D:\Imperial Records\Labs`.
- Normalized current README and PATH guidance to reflect the standalone Sourcebook taxonomy after the moves.
- Simplified `Personal Wikipedia` by removing six unused placeholder subfolders and shifting the evergreen guidance toward a flatter default structure.
- Task type: `vault-governance`
- Added root `AGENTS.md` guidance so future agents must read the local vault rules and record kept edits in this changelog before finishing.
- Replaced the Sourcebook changelog policy with per-edit agent logging instead of notable-only tracking.

### Moved
- Moved `Random Questions/` to `Notes/Random Questions/`.
- Moved `Tips and Trick/` to `Personal Advice/Tips and Trick/`.
- Moved `Idea Backlog/` out of Sourcebook into `D:\Imperial Records\Labs\Idea Backlog/`.

### Workflow
- Updated the installed Obsidian vault skills so `D:\Imperial Sourcebook` now follows this file for every retained agent edit pass, not only larger structural changes.
- Added Sourcebook-specific audit heuristics so future vault audits do not assume the older `Imperial Records` folder layout.
- Updated `PATH.md`, root `README.md`, and `Personal Wikipedia/README.md` so the documented rule now matches the flatter evergreen layout.

### Removed
- Removed the unused `Personal Wikipedia/Book Autopsies/` placeholder folder.
- Removed the unused `Personal Wikipedia/Concept Notes/` placeholder folder.
- Removed the unused `Personal Wikipedia/Domain Wikis/` placeholder folder.
- Removed the unused `Personal Wikipedia/Etymology & Language/` placeholder folder.
- Removed the unused `Personal Wikipedia/Explain It Simply/` placeholder folder.
- Removed the unused `Personal Wikipedia/Scientific Annotations/` placeholder folder.

### Notes
- Counts: 146 markdown notes and 20 supporting files present at bootstrap.
- Counts: 3 folders moved and 12 Sourcebook governance/readme notes updated during the consolidation pass.
- Counts: 1 root agent-instruction file added and 5 installed skill or reference files updated for Sourcebook logging behavior.
- Counts: 6 empty `Personal Wikipedia` placeholder folders and their 6 README files removed.
- Left unresolved: `Personal Advice/Menjadi Expert.md` still references missing file `1000089260.jpg`, which is not present in this vault.
- Left unresolved: the `Quick Note!` duplicate-review pair remains intentionally unchanged.
- Left unresolved: manual edits made outside agent workflows still depend on the editor to add an entry here; this policy only enforces agent-guided work.
- Left unresolved: `Personal Wikipedia/Anti-Library/` remains in place as the only current child bucket.
- Follow-up: none for this pass.
- Follow-up: future same-day agent edits should merge into this `2026-04-22` entry instead of creating another date heading.

---
# Agent Policy

### Ownership

- Only the top-level or orchestrating agent writes the final entry to this file.
- Any top-level agent that keeps file edits under this vault must update this file before finishing unless the run qualifies under `When To Skip Logging`.
- Delegated workers, helper agents, or narrow executor passes must not edit this file directly.
- A task is complete only after its planned edits, cleanup, artifact generation, and verification steps are finished.

### Worker Handoff

If a delegated worker finishes part of a task, it should return a changelog-ready handoff summary to the parent instead of editing this file.

Use this format:

```md
Task type: sourcebook-organization | knowledge-distillation | note-linking | vault-audit | import-cleanup | vault-bootstrap | vault-governance | note-update
Completed: short summary of finished work
Changed: notes, folders, links, rules, or artifacts that changed
Counts: files moved, notes linked, files renamed, findings found, or `none`
Left unresolved: what was intentionally left unchanged, ambiguous, blocked, or incomplete
Follow-up: what should happen next, or `none`
Suggested sections: Changed, Moved, Renamed, Removed, Workflow, Notes
Notable: yes | no
Dry-run: yes | no
```

### When To Log

Write an entry whenever a top-level agent run keeps changes under this vault, including:

- notes, folders, or links changed
- files were created, edited, moved, renamed, or removed
- vault rules, workflows, or templates changed
- a library-wide audit produced saved artifacts or findings worth preserving
- cleanup, linking, or organization work changed even one or two notes
- a partial or blocked run left kept file changes on disk that the next agent should understand

### When To Skip Logging

Skip the changelog update when any of these are true:

- the run was dry-run, preview-only, or planning-only
- the task was delegated work and this agent is not the final owner
- the run ended with no kept file change and no saved artifact
- all temporary edits were reverted before handoff
- a linking or organization pass made no actual vault change
- a read-only review or audit produced no saved artifact and nothing worth preserving here

Do not skip a changelog entry only because the change was small.

### Same-Day Merge

- If a `## YYYY-MM-DD` heading for today already exists, merge the new outcome into that same dated entry.
- Do not create a second heading for the same date.
- Reuse existing sections when they fit.
- Add only the missing bullets for the new completed work.
- Avoid duplicate bullets that restate the same outcome.

## What Belongs Here

Record changes such as:

- large note moves or renames
- small note-level agent edits, summarized briefly when needed
- new root dashboards, indexes, or templates
- changes to vault rules in `PATH.md`, `README.md`, `AGENTS.md`, or this file
- major cleanup or import passes
- changes to study structure, taxonomy, or governance
- audits with material findings or saved artifacts

Usually skip:

- dry-runs, previews, and no-op passes
- delegated worker-only passes that did not own final logging
- read-only reviews with no saved artifact

## How Entries Work

- Use dates instead of software versions.
- Put the newest entry at the top under `## Recent Entries`.
- Keep entries short and specific.
- Focus on what changed and why it matters.
- Use only the sections that apply.
- Merge same-day work into the existing date heading.
- For a one-file or small-note update, a short `Changed` bullet and a short `Notes` bullet are enough. Do not skip it merely because the diff is small.

## Minimum Entry Schema

Every logged task should make these points clear somewhere in the entry:

- task type
- what changed in the vault
- what is already complete
- counts when useful
- what was intentionally left unresolved, unchanged, or blocked
- what follow-up is still recommended

You do not need a dedicated section for each field. The information can be distributed across the normal changelog sections.

## Entry Template

```md
## YYYY-MM-DD

### Changed
- Task type: `task-type`
- Completed: what finished and why it matters

### Moved
- What moved and where it went

### Renamed
- What was renamed and why

### Removed
- What was removed

### Workflow
- Rule, template, plugin, or process changes

### Notes
- Counts: useful numbers if they matter
- Left unresolved: what stayed behind, what was blocked, or what needs follow-up
```

## Suggested Scope By Folder

- `Bahas Soal`: worked examples, formula support, and practice-note organization
- `Notes`: source-driven notes, topical clusters, `Random Questions`, and reference-library cleanup
- `Personal Wikipedia`: evergreen synthesis, glossaries, and durable concept pages
- `Learning & Skills`: technical references, skill maps, and learning systems
- `The Academy`: formal study structures and curriculum-like organization
- `Personal Advice`: practical guidance, rereadable behavioral material, and `Tips and Trick`
- `Design Inspiration` and `Motivation`: supporting reference buckets
- `Attachments`: only notable asset reorganizations or media migrations
- root governance docs: `README.md`, `PATH.md`, `CHANGELOG.md`, and `AGENTS.md`

## Task Examples

### Vault Audit

```md
## 2026-04-22

### Changed
- Task type: `vault-audit`
- Completed a read-only structure audit across Imperial Sourcebook and grouped findings by issue type.

### Workflow
- Saved `audit.json` and `fix-plan.json` for follow-up review.

### Notes
- Counts: 12 findings, 4 direct move suggestions, 8 follow-up items.
- Left unresolved: no notes were moved because the audit pass is read-only.
- Follow-up: run the appropriate organizer workflow on the flagged areas.
```

### Knowledge Distillation

```md
## 2026-04-22

### Changed
- Task type: `knowledge-distillation`
- Distilled source-heavy notes into evergreen concept pages and cleaned the related root navigation.

### Moved
- Promoted 6 notes from `Notes` into `Personal Wikipedia`.

### Notes
- Counts: 6 notes promoted, 3 source notes left in place.
- Left unresolved: 3 notes still need manual review before they are safe to rewrite as evergreen material.
- Follow-up: revisit the remaining notes after another reading pass.
```

### Note Linking

```md
## 2026-04-22

### Changed
- Task type: `note-linking`
- Added or refreshed internal links across the strongest related notes in the same topic cluster.

### Workflow
- Verified the link plan after apply and left weakly related notes unchanged.

### Notes
- Counts: 11 notes updated, 27 links added, 6 notes left unlinked.
- Left unresolved: some notes still need cleanup before they are safe to link more aggressively.
- Follow-up: clean malformed or noisy notes, then run another linking pass.
```
