# Matematika Dasar

`Matematika Dasar` stores topic-grouped practice material for basic math problem solving inside `Bahas Soal`. Keep each topic folder focused on one math topic, then place new practice files under that topic instead of creating a broad mixed folder.

## What Belongs Here

- topic folders such as `Bilangan Berpangkat dan Bentuk Akar`
- LaTeX source files for `Set N` and `Kuis N`
- final PDFs when they are useful for printing or review
- answer keys or worked-solution notes when they stay tied to the same problem topic

## What Does Not

- broad theory notes that are not tied to practice material
- unrelated UTBK or non-basic-math practice material
- empty topic buckets, answer-only files, or attachment-only records
- build intermediates such as `.aux`, `.log`, and `.synctex.gz` after they are no longer needed

## Folder Pattern

Use one folder per problem topic.

```text
Matematika Dasar/
  Template Set Kuis.tex
  [Problem Topic]/
    Set/
      Set N.tex
      Set N.pdf
    Kuis/
      Kuis N.tex
      Kuis N.pdf
```

The current tree may contain legacy all-caps `SET/` folders. Do not rename them during ordinary problem creation. For new topic folders, prefer `Set/` and `Kuis/` so folder names follow the vault naming convention.

## Naming Rules

- Use `Set N.tex` for open-ended practice sets.
- Use `Kuis N.tex` for multiple-choice quizzes.
- Let `N` count within the same topic and material type.
- Keep the matching PDF stem identical when exporting, such as `Set 2.tex` and `Set 2.pdf`.
- Use title-case English topic names and sentence-case Indonesian topic names.

## Problem Sheet Format

Every file should start with a simple header:

```text
Set N - Matematika Dasar
[Problem Topic]
Tanggal: Hari - DD/MM/YYYY
Tingkat: easy / intermediate / difficult
```

For `Kuis`, use:

```text
Kuis N - Matematika Dasar
[Problem Topic]
Tanggal: Hari - DD/MM/YYYY
Tipe: Pilihan ganda, campuran intermediate-difficult
```

## Set Rules

- Use open-ended questions only.
- Pick one difficulty label when the whole file has one level.
- If one file intentionally contains multiple levels, split it with short sections such as `Tingkat easy`, `Tingkat intermediate`, and `Tingkat difficult`.
- Keep question numbering continuous unless a separate section needs its own numbering.

## Kuis Rules

- Use multiple-choice questions with five options: `A` through `E`.
- Mix intermediate to difficult questions unless a task explicitly asks for another range.
- Keep options short and parallel when possible.
- Do not include the answer key inside the student-facing sheet unless the file is explicitly marked as a key or solution version.

## Template Use

Use `Template Set Kuis.tex` as the starting point for both material types.

1. Copy the template into the correct topic and material folder.
2. Rename it to `Set N.tex` or `Kuis N.tex`.
3. Leave `\kuisfalse` for a `Set`; change it to `\kuistrue` for a `Kuis`.
4. Replace `N`, `[Problem Topic]`, the date, and the placeholder problems.
5. Compile to PDF only after the source file title and folder location are final.

## TeXstudio Build Setup

TeXstudio creates helper files such as `.aux`, `.log`, and `.synctex.gz` every time a file is compiled. Keep those files out of the problem folder by sending build output to a local `build/` folder.

Recommended TeXstudio command:

```text
latexmk -pdf -interaction=nonstopmode -synctex=1 -outdir=build %.tex
```

Use this in TeXstudio through `Options > Configure TeXstudio > Commands > Latexmk`, then set the default compiler to `Latexmk` in `Build`.

If TeXstudio cannot open the PDF or log after compiling, enable advanced options and add `build` under `Options > Configure TeXstudio > Build > Build Options > Additional Search Paths` for both PDF files and log files.

If using raw `PdfLaTeX` instead:

```text
pdflatex -synctex=1 -interaction=nonstopmode -output-directory=build %.tex
```

For raw `PdfLaTeX`, create the `build/` folder beside the `.tex` file before compiling. `latexmk` is preferred here because it creates the `build/` folder automatically and keeps repeated compiles tidier.

Use `Tools > Clean Auxiliary Files` in TeXstudio to remove old helper files from folders that were compiled before this setup.

## Review Rhythm

Review this folder when new problem topics repeat, when a topic accumulates several numbered files, or when generated LaTeX build files start crowding the topic folders.
