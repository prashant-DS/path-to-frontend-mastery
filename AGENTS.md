# AGENTS.md

Guidance for AI agents contributing to **Path to Frontend Mastery**.

## What this repo is

A personal, first-person knowledge base documenting one engineer's path from junior to
senior frontend. It is **content, not software**: there is no `package.json`, no build
step, no test suite, no linter. Everything is Markdown (plus occasional images).

Do not introduce tooling, CI, generators, or a static-site framework unless explicitly
asked. Adding a build system to a notes repo is the most likely way to get this wrong.

## Structure

```
README.md                          Repo intro / manifesto
AGENTS.md                          This file
myInterviews/                      Real interview retrospectives
  <role>(<years>y)/                e.g. senior-fe-engineer(5y)
    <company>/                     camelCase company name, e.g. waltDisney
      R1.md, R2.md, ...            One file per round, in order
systemDesign/                      System design notes (currently images only)
```

Conventions to preserve:

- Role folders encode seniority and YOE: `senior-fe-engineer(5y)`.
- Company folders are camelCase, no spaces: `rafaySystem`, `waltDisney`.
- Round files are `R<n>.md`, numbered in the order the rounds happened.
- Assets live next to the notes that reference them.

## Writing style

The voice is a personal retrospective, not a tutorial and not a textbook.

- **First person, past tense.** "Was asked to…", "I decided to…", "We spent roughly
  30 minutes…". Never write in second person ("you should…") or marketing voice.
- **Honest.** Record what actually happened, including what went badly, what was
  missed, and what the interviewer pushed back on. Do not invent outcomes, timings,
  interviewer reactions, or details that were not supplied.
- **Concept-first.** After the question, explain _why_ the answer is what it is
  ("Key concepts:", "### Approach"), rather than only dumping a solution.
- **Self-contained examples.** Each question should carry an input/output example rich
  enough that a reader could attempt the problem from the note alone. For a data
  transformation, cover the interesting cases (primitives, nesting, arrays, empties),
  not just the trivial one.
- **Mark what is not remembered.** Rounds done on paper or whiteboard often have no
  saved artefact. Say so inline ("I don't remember the exact input — this is the same
  shape") rather than presenting a reconstruction as fact.
- No emojis. No exclamation-heavy filler. No "In this article, we will explore…".

## Markdown formatting

Match the existing files:

- One `#` H1 at the top naming the round and format, e.g.
  `# HackerRank React Assessment — Round 2` or
  `# System Design + Frontend Implementation — Round 2`.
- An `## Overview` or `## Setup` section describing the round's format.
- `---` horizontal rules between major sections.
- Numbered `### N. <Question title>` for individual questions within a round.
- Fenced code blocks **with a language tag**: `js`, `jsx`, `text` for outputs/diagrams.
- Use `text` fences for expected console output and ASCII diagrams.

## When adding a new interview write-up

1. Create/reuse `myInterviews/<role>(<Ny>)/<companyCamelCase>/`.
2. Add `R<n>.md` for the round.
3. Include, where known: round format and platform (HackerRank, plain editor, live
   pairing, pen and paper), the questions asked, the code as given and as written, the
   approach and key concepts, and anything the interviewer emphasised or pushed back on.
4. Do not fabricate missing pieces — omit the section instead, or mark it explicitly
   as a gap.
5. Ask before inventing code the author only described verbally. Prefer prose about the
   approach over a plausible-looking implementation they never wrote.

## Extending the repo

`systemDesign/` and the README's "What's Inside" list (things I wish I knew earlier,
production patterns, mistakes, deep dives) are the intended growth areas. When adding
a new top-level topic, create a directory in the same lowerCamelCase style and follow
the same Markdown conventions.

## Do not

- Rewrite existing notes into a neutral/impersonal voice.
- Add frontmatter, badges, tables of contents, or nav scaffolding unasked.
- Add summary/changelog Markdown files describing your own edits.
- Reformat files you were not asked to touch.
