# Matematika Dasar

`Matematika Dasar` stores topic-grouped basic math practice material inside `Bahas Soal`. Markdown is the core file format for this folder so problem sets stay clean, readable, and easy to edit in Obsidian or any text editor.

## What Belongs Here

- topic folders such as `Bilangan Berpangkat dan Bentuk Akar`
- Markdown source files for `Set N` and `Kuis N`
- answer keys or worked-solution notes when they stay tied to the same problem topic
- optional exported files only when they support a Markdown source file

## What Does Not

- broad theory notes that are not tied to practice material
- unrelated UTBK or non-basic-math practice material
- empty topic buckets, answer-only files, or attachment-only records
- generated build files or editor output that distracts from the Markdown source

## Folder Pattern

Use one folder per problem topic.

```text
Matematika Dasar/
  Template Set.md
  Template Kuis.md
  [Problem Topic]/
    Set/
      Set N.md
      Set N - Pembahasan.md
    Kuis/
      Kuis N.md
      Kuis N - Kunci.md
```

## Naming Rules

- Use `Set N.md` for open-ended practice sets.
- Use `Kuis N.md` for multiple-choice quizzes.
- Let `N` count within the same topic and material type.
- Use `Set N - Pembahasan.md` for worked solutions.
- Use `Kuis N - Kunci.md` for answer keys and short explanations.
- Use title-case English topic names and sentence-case Indonesian topic names.

## Problem Sheet Format

Every file should start with a simple header:

```md
# Set N - Matematika Dasar

Topik: [Problem Topic]
Tanggal: Hari - DD/MM/YYYY
Tingkat: easy / intermediate / difficult
```

For `Kuis`, use:

```md
# Kuis N - Matematika Dasar

Topik: [Problem Topic]
Tanggal: Hari - DD/MM/YYYY
Tipe: Pilihan ganda
Tingkat: campuran intermediate-difficult
```

## Set Rules

- Use open-ended questions only.
- Pick one difficulty label when the whole file has one level.
- If one file intentionally contains multiple levels, split it with short sections such as `### Tingkat easy`, `### Tingkat intermediate`, and `### Tingkat difficult`.
- Keep question numbering continuous unless a separate section needs its own numbering.
- Use display math with `$$ ... $$` for expressions that should stand alone.

## Kuis Rules

- Use multiple-choice questions with five options: `A` through `E`.
- Mix intermediate to difficult questions unless a task explicitly asks for another range.
- Keep options short and parallel when possible.
- Do not include the answer key inside the student-facing sheet unless the file is explicitly marked as a key or solution version.

## Template Use

Use `Template Set.md` for open-ended practice and `Template Kuis.md` for multiple-choice practice.

1. Copy the matching template into the correct topic and material folder.
2. Rename it to `Set N.md` or `Kuis N.md`.
3. Replace `N`, `[Problem Topic]`, the date, and the placeholder problems.
4. Keep answers in a separate `Pembahasan` or `Kunci` file when they are needed.
5. Check the note in Obsidian Reading view so the math renders cleanly.

## Markdown Math Rules

- Use inline math for short expressions such as `$x > 3$`.
- Use display math for main problem expressions:

```md
$$
\sqrt{48}+\sqrt{75}-\sqrt{27}
$$
```

- Keep each problem readable in plain text before relying on rendered math.
- Avoid layout tricks that only make sense in printed documents.

## Review Rhythm

Review this folder when new problem topics repeat, when a topic accumulates several numbered files, or when answer keys and worked solutions need to be split from student-facing questions.
