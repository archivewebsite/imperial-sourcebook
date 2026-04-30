# Bahas Soal Templates

`Templates` defines the global practice-file standard for every new problem file created under `Bahas Soal`. Use these templates when a subject folder does not have a stricter local template, and keep local templates compatible with the shared header and quality controls here.

## Core Rule

Every future practice file should share the same planning header and quality controls. The body changes by practice type.

## Universal Header

Use this shape at the top of every student-facing practice file:

```md
# [Tipe] N - [Bidang]

- Bidang: [Matematika Dasar / Penalaran Matematika / Pengetahuan Kuantitatif / Other]
- Topik: [Problem Topic]
- Fokus keterampilan: [Skill focus]
- Tanggal: Hari - DD/MM/YYYY
- Tipe: [Set / Kuis / Drill / Paket Stimulus]
- Tingkat: easy / intermediate / difficult / mixed
- Jumlah soal: [N]
- Estimasi waktu: [minutes] menit
- Companion: `[Matching Kunci or Pembahasan file].md`
```

## Practice Types

- `Set`: open-ended practice without multiple-choice options.
- `Kuis`: multiple-choice practice, usually with five options.
- `Drill`: rapid repetition of one micro-skill.
- `Paket Stimulus`: UTBK-style stimulus packet with one shared stimulus and several related questions.
- `Pembahasan`: worked solution companion file.
- `Kunci`: compact answer key companion file.

## Decision Rule

- Need open-ended topic practice? Use `Template Set.md`.
- Need multiple choice? Use `Template Kuis.md`.
- Need rapid repetition of one micro-skill? Use `Template Drill.md`.
- Need one passage, table, chart, rule set, or scenario for several questions? Use `Template Paket Stimulus.md`.
- Need full worked reasoning? Use `Template Pembahasan.md`.
- Need compact answers only? Use `Template Kunci.md`.

## Quality Controls

Before saving a new practice file:

- `Jumlah soal` matches the actual number of questions.
- `Kisi-Kisi` matches the real distribution of topics, formats, and difficulty.
- Student-facing files do not contain answers.
- Each question has a clear `Materi` or focus label when the file mixes topics.
- Kuis options are parallel and plausible.
- Drill files train one micro-skill only.
- Paket Stimulus questions all depend on the shared stimulus.
- Math renders cleanly in Obsidian Reading view.
- Companion `Kunci` or `Pembahasan` file is named in the header.

## Reference Examples

Use these Inbox folders as examples of good question style and UTBK-style variation, not as templates:

- `Inbox/contoh soal penalaran matematika`
- `Inbox/contoh soal pengetahuan kuantitatif`

See `Practice Question Guidelines.md` for the patterns extracted from those examples.

