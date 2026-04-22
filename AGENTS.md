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
