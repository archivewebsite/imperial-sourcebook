# Vocabulary

`Vocabulary` stores German-Indonesian and Indonesian-German translated-word dictionaries for language review.

## What Belongs Here

- German-Indonesian vocabulary tables
- Indonesian-German vocabulary tables
- translated word lists with source word, translation, part of speech, comprehension level, review status, and notes

## How To Use It

- keep each dictionary as a plain Markdown table so it renders cleanly in Obsidian
- keep this folder only for German-Indonesian and Indonesian-German vocabulary
- use one row per word or phrase
- name dictionary files as `Vocabulary n.md`, where `n` is the file number
- keep a maximum of 100 vocabulary rows per dictionary file
- when `Vocabulary n.md` reaches 100 vocabulary rows, create `Vocabulary n+1.md` and continue there
- split dictionaries by class or source only when retrieval improves

## Table Schema

Column order for every dictionary:

`Word | Translation | Part of Speech | Comprehension Level | To Review | Notes`

## Column Options

`Comprehension Level` tracks how well the word is understood.

- `Unfamiliar`: the word is new or cannot be recognized without help.
- `Familiar`: the word can be recognized in context, but still needs review.
- `Mastered`: the word can be understood reliably without checking.

`To Review` controls whether the word stays in active review.

- `Yes`: keep the word in active review.
- `No`: keep the word as reference, but remove it from active review.
