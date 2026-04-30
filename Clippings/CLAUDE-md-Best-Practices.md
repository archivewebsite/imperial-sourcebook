---
title: "CLAUDE.md Best Practices"
author: "Nick Babich"
site: "UX Planet"
published: 2026-03-06T18:16:58Z
source: "https://uxplanet.org/claude-md-best-practices-1ef4f861ce7c"
domain: "uxplanet.org"
language: "en"
description: "CLAUDE.md Best Practices 10 Sections to Include in your CLAUDE.md CLAUDE.md is a critical file for providing project-specific context to Claude Code. It serves an onboarding guide for AI to your …"
word_count: 1791
---

## [UX Planet](https://uxplanet.org/?source=post_page---publication_nav-819cc2aaeee0-1ef4f861ce7c---------------------------------------)

Follow publication

[![UX Planet](https://miro.medium.com/v2/resize:fill:76:76/1*A0FnBy5FBoVQC02SZXLXPg.png)](https://uxplanet.org/?source=post_page---post_publication_sidebar-819cc2aaeee0-1ef4f861ce7c---------------------------------------)

UX Planet is a one-stop resource for everything related to user experience.

Follow publication

![](https://miro.medium.com/v2/resize:fit:1400/format:webp/1*grkcAnwIvZ62EI_cy4KSSA.png)

## 10 Sections to Include in your CLAUDE.md

`CLAUDE.md` is a critical file for providing project-specific context to Claude Code. It serves an onboarding guide for AI to your project requirements and codebase. Whenever Claude’s AI model writes new or modifies existing code in your project, the first thing it will do is check the Claude.md file.

In this article, I will share everything you need to know to craft a great `CLAUDE.md` file and streamline your coding process.

## File location, file format and how Claude AI uses it

`CLAUDE.md` file is typically placed in the root of the project repository. For example, if you’re working with the React web app, you should have this structure.

![](https://miro.medium.com/v2/resize:fit:1144/format:webp/1*TFhi8ipJAPXeGFP-mxFTfA.png)

CLAUDE.md file location

The file itself is structured in markdown format (.md stands for markdown).

```c
## Project Overview
Short explanation of what the project is.

## Tech Stack
- TypeScript
- Next.js
- Tailwind
- ShadCN

## Architecture
Explain folders and patterns.

## Coding Rules
- Use functional React components
- Prefer server components
- Use Tailwind utilities instead of custom CSS

## Design System
- Follow ShadCN patterns
- Use tokens from /styles/tokens.ts

## Commands
npm run dev
npm run build
```

Anthropic’s docs say `CLAUDE.md` is part of Claude Code’s project memory, loaded at the start of each conversation, and that Claude treats it as *context rather than hard enforcement.*

## Common sections

Although every project is different, and it’s impossible to provide a one-size-fits-all structure for `CLAUDE.md` file, it is still possible to name 10 key sections that will be relevant to most projects:

## 1\. Project overview

This is the highest-value section that creates context for Claude. In this section, you should explain in plain language:

- What the product is
- Who it is for
- What the app is trying to optimize for
- Most important business or UX constraints

### Best practices

Keep this to a few paragraphs. Claude does better with a crisp mental model than with a long brand story.

❌ Bad:

- long origin story with a lot of historical facts about the company
- generic statements like “we value innovation”
- marketing copy with no implementation relevance

✅ Good:

- “This is a B2B analytics dashboard for operations managers.”
- “Primary goal: reduce time-to-insight.”

### Example

```c
## Project Overview
This project is a web app for product designers to generate 
and refine landing pages with AI.

Primary users are startup founders and marketers who want
high-quality output fast.

The product optimizes for:
- visual polish
- speed of iteration
- clean responsive code
- easy handoff to engineering

Avoid over-engineering. Prefer clarity over cleverness.
```

### 💡 Pro tip

Write this section so Claude can answer:

> “What kind of product is this, and what should it optimize for?”

## 2\. Tech stack

This section prevents a lot of bad assumptions. Without this section, Claude may introduce libraries that are technically valid but wrong for your project.

State the actual technologies in use:

- framework
- programming language
- styling system
- component library
- state management
- testing frameworks
- build tooling
- backend/data layer if relevant

### Best practices

Be explicit. Don’t write “React stack” when you really mean “Next.js App Router + TypeScript + Tailwind + shadcn/ui + Supabase”.

Also include what **NOT** to use.

### Example

```c
## Tech Stack
- Next.js 15 with App Router
- TypeScript
- Tailwind CSS
- shadcn/ui
- React Hook Form + Zod for forms
- Supabase for auth and data
- Vitest for unit tests

Do not introduce:
- Redux
- styled-components
- Material UI
unless explicitly requested.
```

## 3\. Architecture

This is where you teach Claude how the repo is organized.

You need to describe:

- major directories
- responsibilities of each area
- data flow
- separation of concerns
- where new code should go

### Best practices

Focus on decision rules, not just folder names.

❌ Bad:

```c
src/components contains components
```

✅ Good:

```c
Use \`src/components/ui\` for reusable presentational components.
Use \`src/features/*\` for domain-specific UI and logic.
Keep API calls out of presentational components.
```

### Example

```c
## Architecture
- \`app/\` contains routes and server components
- \`components/ui/\` contains reusable design-system components
- \`components/marketing/\` contains landing-page sections
- \`lib/\` contains utilities, API helpers, and shared config
- \`features/\` contains feature-specific business logic
- \`types/\` contains shared TypeScript types

Rules:
- Keep page-level composition in route files
- Move repeated UI into reusable components
- Keep side effects out of UI components when possible
- Prefer server-side data fetching unless client interactivity is required
```

### 💡Pro tip

Add a short “ *where new things go* ” subsection. That helps a lot for project refinement.

### ⚠️ ️Important

If you use API calls to 3rd party services and need to store API keys to access the tools, it’s recommended to keep the keys it in a specific file in the root folder of your project:

```c
.env
```

Apart from that, you should provide a clear instruction to Claude Code on where the API keys are located:

```c
API keys are stored in '.env'
```

This instruction will prevent Claude from storing the keys in random places and minimize the risk that the keys will be exposed.

## 4\. Coding conventions

Along with the project overview, I think that this is the second most important section in the whole file because it has a direct impact on the quality of code output produced by Claude. It defines whether the code is readable and clear for anyone who will read it.

You need to include anything that impacts day-to-day code generation:

- naming conventions
- component patterns
- typing standards
- file size preferences
- import conventions
- error handling
- comments
- async patterns

### Best practices

Use clear rules, not vague preferences.

❌ **Weak:**

```c
"Write clean code"
```

✅ **Strong:**

```c
"Use named exports except for route files"

"Avoid any; prefer inferred types or explicit interfaces"

"Keep components under 200 lines unless justified"
```

### Example

```c
## Coding Conventions
- Use TypeScript strictly; avoid \`any\`
- Prefer functional components
- Prefer named exports for shared modules
- Use async/await instead of chained promises
- Keep components focused and composable
- Extract repeated logic into hooks or helpers
- Prefer descriptive variable names over abbreviations
- Add comments only when intent is non-obvious
- Do not leave dead code or commented-out blocks
```

### 💡 Pro tip

Make rules actionable enough that Claude can follow them automatically.

## 5\. UI and design system rules

For frontend projects, this section is gold.

Define:

- visual style
- spacing philosophy
- typography approach
- interaction patterns
- responsiveness
- accessibility expectations
- component usage rules

### Example

```c
## UI and Design Rules
- Use shadcn/ui primitives as the default foundation
- Prefer spacious layouts and strong visual hierarchy
- Use restrained color usage; rely on typography, spacing, and contrast
- Prefer 8px spacing rhythm
- Buttons should have clear primary/secondary hierarchy
- Forms should be short, scannable, and mobile-friendly
- Every interactive element must have visible hover, focus, and disabled states
- Meet accessibility expectations for contrast, labels, and keyboard navigation
```

### 💡 Pro tip

If you want to achieve a particular look and feel in your design, don’t just say “ *make it modern* ”. That means nothing operationally. Always translate style into implementation guidance.

## 6\. Content and copy guidance

This section is underrated, especially for landing pages and product work.

State how copy should sound:

- concise or detailed
- technical or plain language
- aspirational or practical
- sentence length
- headline style
- forbidden patterns

### Best practices

Include examples of what good copy looks like for your product. Provide link to your existing brand guidelines with tone and voice.

### Example

```c
## Content Guidelines
- Use concise, confident language
- Avoid hype and empty marketing phrases
- Headlines should be clear before clever
- Body copy should focus on user outcomes
- Prefer short paragraphs and scannable structure
- Avoid jargon unless the audience clearly expects it
```

## 7\. Testing and quality bar

Claude should know how finished work is validated.

Define:

- what tests to add
- when tests are required
- lint/typecheck expectations
- what “done” means

### Example

The following set of actions will prevent Claude from under-testing and over-testing:

```c
## Testing and Quality
Before considering a task complete:
- run typecheck
- run lint
- run relevant tests for modified logic

Testing rules:
- add unit tests for reusable logic
- do not add heavy test scaffolding for simple presentational sections
- ensure responsive behavior for UI changes
- verify empty, loading, and error states where relevant
```

### 💡 Pro tip

You can test not only functional, but business logic too.

## 8\. File and component placement rules

This deserves its own section because it stops repo drift. The section is especially useful in mature repos where duplicate components become a problem fast.

You need to define rules for:

- where to create new files
- when to edit existing files
- when to create abstractions
- naming patterns

### Example

```c
## File Placement Rules
- Add new landing-page sections to \`components/marketing/sections\`
- Add reusable primitives to \`components/ui\`
- Put shared helpers in \`lib\`
- Do not create a new abstraction for one-off usage
- Prefer editing existing components over creating near-duplicates
```

## 9\. Safe-change rules

Very valuable for real projects. Its a good idea to tell Claude what it should avoid changing casually. It reduces “ *technically smart but operationally risky* ” edits that will lead to pricy refactoring.

### Example

```c
## Safety Rules
- Do not rename public API routes unless explicitly requested
- Do not change database schema without calling it out clearly
- Do not modify auth flows unless the task requires it
- Preserve backward compatibility for shared components
- Flag major architectural changes before implementing them
```

## 10\. Specific Commands

Anthropic’s recommends giving Claude concrete project context, and commands are part of that operational context.

Add the actual commands Claude should use (like *install, dev, build, lint, test, format, storybook (if relevant), SQL database commands if safe*)

Of course, only include commands that are real and current.

### Example

```c
## Commands
- Install: \`pnpm install\`
- Dev: \`pnpm dev\`
- Build: \`pnpm build\`
- Lint: \`pnpm lint\`
- Typecheck: \`pnpm typecheck\`
- Test: \`pnpm test\`
```

## Example of CLAUDE.md file for a landing page design

Here is a quick preview of how `CLAUDE.md` will look like for a web project (landing page) crafted with React framework:

![](https://miro.medium.com/v2/resize:fit:1400/format:webp/1*y_qtVYZUVyBmhoyiqnxyqg.gif)

Preview of a file for a real project

## Want to master Claude Code?

Check out my complete guide to Claude Code, packed with highly practical insights on how you can integrate it into your design process.

## [Claude Code: Practical Guide for Product Designers](https://babich.gumroad.com/l/claude?source=post_page-----1ef4f861ce7c---------------------------------------)

### Practical guide for product designers who want to master Claude CodeIt covers following topics: Claude Code Best…

babich.gumroad.com

## Responses (21)

Raja Premium 88

```c
How about an example with all sections
```

23

Reply

```c
its not a good exemaple; max 100 line; use rules for patterns
```

20

Reply

```c
Excellent writing! I learned a lot from this—thanks so much for sharing.
```

14

Reply
