# Changelog

All notable changes to Imperial Sourcebook should be documented here.

This changelog is adapted for a personal knowledge vault, not a software product. It tracks meaningful changes to structure, organization, workflows, and library-wide documentation. It does not need to record every small wording edit inside individual notes.

## Recent Entries

Add new dated entries at the top of this section.

## 2026-04-22

### Changed
- Task type: `vault-bootstrap`
- Connected the local `D:\Imperial Sourcebook` vault to the GitHub repository `https://github.com/archivewebsite/imperial-sourcebook.git`.
- Replaced the legacy root `README.md` from the old `Resources` folder with Sourcebook-specific root documentation.
- Added `PATH.md`, `CHANGELOG.md`, `.gitignore`, and the remote `LICENSE` so the vault has the same root governance pattern as `Imperial Records`.

### Notes
- Counts: 146 markdown notes and 20 supporting files present at bootstrap.
- Left unresolved: `Personal Advice/Menjadi Expert.md` still references missing file `1000089260.jpg`, which is not present in this vault.
- Follow-up: update subfolder README references that still mention `Resources/...` if you want the wording fully normalized to the standalone vault.

---
# Agent Policy

### Ownership

- Only the top-level or orchestrating agent writes the final entry to this file.
- Delegated workers, helper agents, or narrow executor passes must not edit this file directly.
- A task is complete only after its planned edits, cleanup, artifact generation, and verification steps are finished.

### Worker Handoff

If a delegated worker finishes part of a task, it should return a changelog-ready handoff summary to the parent instead of editing this file.

Use this format:

```md
Task type: sourcebook-organization | knowledge-distillation | note-linking | vault-audit | import-cleanup | vault-bootstrap
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

Write an entry only when the completed task produced notable outcomes such as:

- notes, folders, or links changed
- files were moved, renamed, or removed
- vault rules, workflows, or templates changed
- a library-wide audit produced material findings or saved artifacts
- import cleanup changed how the vault is organized or used

### When To Skip Logging

Skip the changelog update when any of these are true:

- the run was dry-run, preview-only, or planning-only
- the task was delegated work and this agent is not the final owner
- the task produced no notable completed outcome
- the task ended early, was blocked, or was not verified
- a linking pass found no strong links and produced no meaningful reviewed outcome worth recording
- an organization pass made no actual vault change

### Same-Day Merge

- If a `## YYYY-MM-DD` heading for today already exists, merge the new outcome into that same dated entry.
- Do not create a second heading for the same date.
- Reuse existing sections when they fit.
- Add only the missing bullets for the new completed work.
- Avoid duplicate bullets that restate the same outcome.

## What Belongs Here

Record changes such as:

- large note moves or renames
- new root dashboards, indexes, or templates
- changes to vault rules in `PATH.md` or `README.md`
- major cleanup or import passes
- changes to study structure, taxonomy, or governance
- audits with material findings or saved artifacts

Usually skip:

- typo fixes
- small wording edits inside a single note
- normal note-taking
- routine additions of one or two notes
- dry-runs, previews, and no-op passes

## How Entries Work

- Use dates instead of software versions.
- Put the newest entry at the top under `## Recent Entries`.
- Keep entries short and specific.
- Focus on what changed and why it matters.
- Use only the sections that apply.
- Merge same-day work into the existing date heading.

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
- `Notes`: source-driven notes, topical clusters, and reference-library cleanup
- `Personal Wikipedia`: evergreen synthesis, glossaries, and durable concept pages
- `Learning & Skills`: technical references, skill maps, and learning systems
- `The Academy`: formal study structures and curriculum-like organization
- `Personal Advice`: practical guidance and rereadable behavioral material
- `Idea Backlog` and `Random Questions`: future ideas and open curiosities
- `Design Inspiration`, `Motivation`, and `Tips and Trick`: supporting reference buckets
- `Attachments`: only notable asset reorganizations or media migrations

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
