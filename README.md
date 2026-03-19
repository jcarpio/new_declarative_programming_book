# Declarative Programming — Book Project

> **A complete revision of the original teaching material**, restructured in the style of the *For Dummies* series, covering both **Haskell** (functional programming) and **Prolog** (logic programming).
>
> *José Carpio Cañada · Gonzalo Antonio Aranda Corral · José Marco de la Rosa*
> *Universidad de Huelva · Teaching Books [95] · 2021*

---

## Table of Contents

- [Project Overview](#project-overview)
- [Original Book](#original-book)
- [Translation Work](#translation-work)
- [New Edition: For Dummies Restructure](#new-edition-for-dummies-restructure)
- [Book Structure](#book-structure)
- [Illustration Style Guide](#illustration-style-guide)
- [AI Image Generation Prompts](#ai-image-generation-prompts)
- [Deliverables](#deliverables)
- [How to Use This Repository](#how-to-use-this-repository)
- [Contributing](#contributing)

---

## Project Overview

This repository documents the full revision process of a university-level **Declarative Programming** textbook. The original book was written in Spanish and used in courses at the Universidad de Huelva. The project covers:

1. **Full English translation** of all untranslated sections (the original PDF was partially translated).
2. **Structural reorganisation** of the content following the *For Dummies* editorial philosophy.
3. **New exercises** added to every chapter, with progressive difficulty.
4. **Illustration brief** for hand-drawn sketch characters inspired by *La disciplina de emprender* (Bill Aulet).

The goal is a book that is **genuinely fun to read**, accessible to students with no prior background in declarative programming, and rigorous enough for use in a university course.

---

## Original Book

### Content

The original book (`N_95_en_v5.pdf`) covers **148 pages** divided into:

| Section | Language in original | Topics |
|---|---|---|
| Front matter (pp. 1–17) | ✅ English | Introduction, acknowledgements, paradigms, bibliography |
| Haskell Theory (pp. 21–40) | ❌ Spanish | Sections 0–9: intro, functions, operators, lazy eval, HOF, currying, composition, lists, patterns, tuples |
| Haskell Recursion (pp. 43–48) | ✅ English | Section 10: recursion, foldl, induction |
| Prolog Intro (pp. 51–64) | ✅ English | Introduction, variables, unification operators |
| Prolog Lists (pp. 65–75) | ✅ English | Lists, `num_elem`, reversible predicates |
| Prolog Lists cont. (pp. 76–112) | ❌ Spanish | Sorting algorithms, trees, graphs, execution control, state problems |
| Practices — Haskell (pp. 113–130) | ❌ Spanish | Hugs setup, lists, patterns/tuples/recursion, exam exercises |
| Practices — Prolog (pp. 131–148) | ❌ Spanish | SWI-Prolog setup, simple predicates, list predicates, trees, graphs |

### Predicate / Function Name Translation Table

All Prolog predicate names and Haskell function names were translated from Spanish to English during the translation process:

| Spanish | English |
|---|---|
| `inserta_en_list_ord` | `insert_in_sorted_list` |
| `ordena_insercion` | `insertion_sort` |
| `ordena_quick` | `quick_sort` |
| `lista_divisores` | `list_divisors` |
| `primo` / `primosEntrexy` | `prime` / `primes_between` |
| `selecciona_uno` / `permuta` | `select_one` / `permute` |
| `mas_veces` | `most_frequent` |
| `cuenta_nodos` / `lista_hojas` | `count_nodes` / `list_leaves` |
| `profundidad_ag` | `depth_gt` |
| `arista` / `grafo` / `dato` | `edge` / `graph` / `datum` |
| `camino` / `conectado` / `visitado` | `path` / `connected` / `visited` |
| `pasar` / `mov` / `solucion` | `cross` / `mov` / `solution` |
| `inicial` / `final` / `estado` | `initial` / `final` / `state` |

---

## Translation Work

### Files Produced

| File | Contents | Pages covered |
|---|---|---|
| `prolog_translation_en.docx` | Prolog theory sections: list algorithms, binary & generic trees, graphs, execution control (cut, repeat, fail, resolution trees), state problems (missionaries & cannibals) | pp. 76–112 |
| `remaining_translation_en.docx` | Haskell theory (sections 0–9), all Haskell practices, all Prolog practices | pp. 21–40, 113–148 |
| `declarative_programming_complete_en.docx` | **Full book** — all sections in English in a single document | pp. 1–148 |

### Translation Notes

- All **code comments** were translated from Spanish to English.
- All **predicate and function names** were renamed to English equivalents (see table above).
- Minor errors found in the original text (e.g. incorrect variable names in a few code examples) were silently corrected.
- Sections already in English in the original were kept verbatim, with only minor editorial improvements.

---

## New Edition: For Dummies Restructure

### Philosophy

The *For Dummies* series is built around a set of editorial principles that make technical content approachable:

| Principle | How it's applied in this book |
|---|---|
| **Talk to the reader directly** | "You" language throughout. No passive voice. |
| **Lead with "why", not "what"** | Every chapter opens with motivation before syntax. |
| **Analogies over abstractions** | "Functional programming is like a spreadsheet formula" before any definition. |
| **Chunked learning** | Short sections. Every concept isolated and named. |
| **In This Chapter box** | Each chapter opens with a checklist of exactly what the reader will learn. |
| **Callout boxes** | 5 types: Tip 💡, Remember 🔖, Warning ⚠️, Technical Stuff 🔧, Try It 🖥️ |
| **The Part of Tens** | Mandatory section: three "Top 10" lists at the end of the book. |
| **Appendices as reference cards** | Haskell quick ref, Prolog quick ref, full glossary. |

### What Changed vs the Original

| Original | New edition |
|---|---|
| Chapter opens with theory | Chapter opens with a real-world analogy |
| Sections numbered 0–10 | Narrative chapter titles ("The Loop That Isn't a Loop") |
| Exercises at the end of sections | Exercises integrated throughout, with progressive difficulty |
| No installation guidance | Full chapter on setting up Hugs and SWI-Prolog |
| Types covered briefly | Types get their own full chapter ("Haskell's Superpower") |
| Practice sessions as exercise lists | Lab sessions with step-by-step guidance |
| No worked solutions | Chapter 19: exam-style exercises with fully worked solutions |
| No glossary | 20-term glossary in Appendix C |
| No reference cards | Appendix A (Haskell) and Appendix B (Prolog) quick reference cards |

---

## Book Structure

```
Declarative Programming for Dummies
│
├── About This Book
│
├── PART 1: Getting Your Head Around Declarative Thinking
│   ├── Chapter 1:  So You Want to Program Differently
│   ├── Chapter 2:  Two Flavours: Functions vs Logic
│   └── Chapter 3:  Setting Up Your Toolbox
│
├── PART 2: Functional Programming with Haskell
│   ├── Chapter 4:  Your First Haskell Functions
│   ├── Chapter 5:  Types — Haskell's Superpower
│   ├── Chapter 6:  Lists: The Bread and Butter of Haskell
│   ├── Chapter 7:  Pattern Matching and Tuples
│   ├── Chapter 8:  Recursion: The Loop That Isn't a Loop
│   ├── Chapter 9:  Higher-Order Functions, Currying, and Composition
│   └── Chapter 10: Lazy Evaluation: Infinite Lists and Other Magic
│
├── PART 3: Logic Programming with Prolog
│   ├── Chapter 11: Logic, Facts, and Rules — Welcome to Prolog
│   ├── Chapter 12: Unification: The Heart of Prolog
│   ├── Chapter 13: Lists in Prolog
│   ├── Chapter 14: Trees and Graphs in Prolog
│   ├── Chapter 15: Controlling Execution: The Cut and Beyond
│   └── Chapter 16: Solving Problems with States
│
├── PART 4: Putting It All Into Practice
│   ├── Chapter 17: Haskell Lab Sessions
│   ├── Chapter 18: Prolog Lab Sessions
│   └── Chapter 19: Exam-Style Exercises with Worked Solutions
│
├── PART 5: The Part of Tens
│   ├── Chapter 20: Ten Classic Declarative Programs You Should Know
│   ├── Chapter 21: Ten Common Mistakes (And How to Fix Them)
│   └── Chapter 22: Ten Resources to Deepen Your Knowledge
│
├── Appendix A: Haskell Quick Reference Card
├── Appendix B: Prolog Quick Reference Card
└── Appendix C: Glossary (20 terms)
```

### Chapter Summary

#### Part 1 — Getting Your Head Around Declarative Thinking

**Chapter 1** introduces the core mental shift: from *how* (imperative) to *what* (declarative). Uses the restaurant analogy ("ordering food vs cooking it yourself"). Covers programming paradigms and gives a first taste of Haskell and Prolog side by side.

**Chapter 2** compares functional and logic programming directly with a side-by-side table covering core concepts, how programs run, typical use cases, and real-world applications.

**Chapter 3** is a hands-on setup chapter: installing Hugs and SWI-Prolog, writing and loading a first program in each language, using the interactive prompt.

#### Part 2 — Functional Programming with Haskell

**Chapter 4** covers function anatomy: type signatures, multiple equations, guards, if-then-else, case, and `where` clauses. Includes 5 new exercises (sign, max3, temperature conversion, leap year, grade converter).

**Chapter 5** covers Haskell's type system: type classes (Eq, Ord, Num, Fractional, Show), type aliases, and reading type signatures confidently. Includes 3 new exercises.

**Chapter 6** covers lists: basic operations, ranges, extended list notation (list comprehensions). Includes 5 new exercises (Pythagorean triples, word filtering, running sum, deduplication, flatten).

**Chapter 7** covers pattern matching: matching on lists, wildcards, pattern aliases with `@`, and tuples. Includes 4 new exercises.

**Chapter 8** covers recursion via the mathematical induction recipe: base case + recursive case. Walks through `numElements` and `foldl` step by step. Includes 5 new exercises (mySum, myMaximum, myZip, myTakeWhile, myGroupBy).

**Chapter 9** covers higher-order functions (`map`, `filter`, `foldr`/`foldl`), currying and partial application, and function composition with `.`. Includes 4 new exercises including a Caesar cipher and a function pipeline.

**Chapter 10** covers lazy evaluation and infinite lists (`[1..]`, Fibonacci, Sieve of Eratosthenes). Includes 3 new exercises.

#### Part 3 — Logic Programming with Prolog

**Chapter 11** introduces facts, rules, queries, and the closed-world assumption. Includes 3 new exercises: a family tree knowledge base, an animal taxonomy, and a movie database.

**Chapter 12** covers unification in depth: the four essential operators (`=`, `==`, `is`, `=:=`), variable scope, and common pitfalls. Includes 3 new exercises.

**Chapter 13** covers Prolog lists: the head|tail pattern, recursive list predicates, and classic list algorithms. Includes 5 new exercises (contains, count, split, interleave, run-length encoding).

**Chapter 14** covers trees (binary and generic, as nested terms) and graphs (edge-clause and graph-term representations, path-finding). Includes 4 new exercises.

**Chapter 15** covers execution control: the resolution algorithm, green vs red cuts, and negation-as-failure (`\+`). Includes 3 new exercises.

**Chapter 16** covers the state-space framework: state representation, move implementation, path predicate, solution predicate. New exercises: Towers of Hanoi, Water Jug problem, 8-puzzle.

#### Part 4 — Putting It All Into Practice

**Chapter 17** organises Haskell practice into 5 progressive labs: Getting Started, List Comprehensions, Recursive Functions, Higher-Order Functions, and Exam-Style Problems. Adds 5 new exam-style exercises including run-length encoding/decoding.

**Chapter 18** organises Prolog practice into 5 progressive labs: Unification and Basic Queries, Recursive List Predicates, Trees, Graphs, and State-Space Problems. Adds the Farmer/Wolf/Goat/Cabbage puzzle, Knight's Tour, and Sudoku.

**Chapter 19** gives a methodology for approaching exam questions in both languages, with two fully worked examples: Longest Common Subsequence (Haskell) and N-Queens (Prolog).

#### Part 5 — The Part of Tens

**Chapter 20** presents 10 classic declarative programs (lazy Fibonacci, Haskell Quicksort, N-Queens, Peano Arithmetic, Parser Combinators, Family Tree Reasoning, MapReduce, Type Inference, Sudoku Solver, Towers of Hanoi).

**Chapter 21** presents the 10 most common beginner mistakes: 5 for Haskell (missing type signature, `=` vs `==`, missing base case, off-by-one, foldr vs foldl) and 5 for Prolog (missing `.`, `=` vs `is`, variable scope confusion, left recursion, overusing the cut).

**Chapter 22** presents 10 resources to go deeper: 5 for Haskell (LYAH, Real World Haskell, Haskell.org, Hoogle, CIS 194) and 5 for Prolog (Art of Prolog, Bratko, 99 Problems, SWI Manual, SWISH).

---

## Illustration Style Guide

Each major chapter will feature one hand-drawn sketch illustration. The style is inspired directly by *La disciplina de emprender* (Bill Aulet, MIT Press).

### Visual Style Characteristics

| Attribute | Specification |
|---|---|
| **Medium** | Black and white ink line drawing |
| **Color** | None — pure monochrome |
| **Shading** | Minimal thin hatching only, no fills |
| **Characters** | Simple cartoon figures with thick-rimmed glasses, expressive faces, exaggerated hair |
| **Typography** | Hand-lettered text integrated into drawings (speech bubbles, labels) |
| **Background** | Clean white, no backgrounds or borders |
| **Tone** | Warm, humorous, never dry or technical |
| **Line weight** | 1.5–2.5px ink strokes, loose and gestural |
| **Composition** | Characters interacting with concepts as physical objects |

### Illustration Map

| Chapter | Concept illustrated | Scene description |
|---|---|---|
| Ch. 1 | Imperative vs Declarative | Two programmers: one frantic with a 5-step checklist, one relaxed pointing at "sorted list" |
| Ch. 4 | Function anatomy | A scientist labelling the parts of a function like a biology diagram |
| Ch. 5 | Type system | A type inspector with magnifying glass checking "papers" at a border checkpoint |
| Ch. 6 | Lists | A train of linked carriages, each carrying one element; the `head:tail` split shown as uncoupling the engine |
| Ch. 7 | Pattern matching | A magical sorting hat routing different list patterns to different "clause rooms" |
| Ch. 8 | Recursion | A professor pointing at nested Russian dolls, the smallest one glowing: "base case = 0 ⭐" |
| Ch. 9 | Higher-order functions | A chef passing a recipe scroll as an ingredient into the `map` machine |
| Ch. 10 | Lazy evaluation | A sleeping programmer with `[1..]` unrolling infinitely beside them; only the elements being `take`n are awake |
| Ch. 11 | Prolog facts & rules | A librarian building a "Book of Knowledge" with `fact.` stamps; a detective asking queries |
| Ch. 12 | Unification | Two puzzle pieces labeled `foo(X,2)` and `foo(1,Y)` clicking together to reveal `X=1, Y=2` |
| Ch. 15 | The Cut | A decision tree with scissors (`✂`) cutting off branches; one green branch leads to a happy character |
| Ch. 16 | State problems | A board game path from START to GOAL; characters as game pieces making `mov` moves |
| Ch. 20 | Part of Tens opener | Ten tiny characters each holding a different classic program |
| Ch. 21 | Common mistakes | A programmer falling into a pit labeled "forgot the `.`"; another tangled in infinite recursion |

---

## AI Image Generation Prompts

Use these prompts with Midjourney, DALL-E 3, or Stable Diffusion to generate chapter illustrations.

### Universal Style Suffix

Append this to **every prompt** to enforce the visual style:

```
Black and white line drawing, hand-drawn ink illustration, simple cartoon character
with thick-rimmed glasses and expressive face, clean white background, minimal
hatching, loose gestural ink strokes, educational textbook sketch style similar to
Bill Aulet "Discipline of Entrepreneurship". No color. No gradients. No photo-realism.
```

For **Midjourney**: add `--style raw --ar 4:3 --v 6` at the end.
For **DALL-E 3**: add *"Pure black and white line art only. No color whatsoever."*
For **Stable Diffusion**: use model `lineart_realistic` or `sketch_style`.

---

### Per-Chapter Prompts

#### Chapter 1 — The Two Paradigms

```
A split scene. Left side: a frustrated programmer with wild hair and thick glasses
holding a numbered checklist (step 1, step 2, step 3...) and pointing anxiously,
speech bubble says "First do THIS, then do THAT!". Right side: a relaxed programmer
smiling and pointing calmly at a simple post-it note that says "sorted list", speech
bubble says "I just want this result!". Educational textbook sketch style.
[+ Universal Style Suffix]
```

#### Chapter 5 — Types

```
A stern customs officer with thick glasses and a cap stands at a checkpoint booth
labeled "TYPE CHECKER". A programmer is trying to pass through holding a value labeled
"1+1". The officer holds up a hand and checks the "papers" (a type signature). Speech
bubble from officer: "Int -> Int -> Bool? Papers, please." Hand-drawn ink sketch,
educational illustration.
[+ Universal Style Suffix]
```

#### Chapter 6 — Lists

```
A cheerful train conductor with thick glasses stands next to a cartoon train. Each
carriage of the train contains one element: [1], [2], [3], [4]. The engine is labeled
"head" and the rest of the train is labeled "tail". The conductor is uncoupling the
engine from the rest, with a smile. Speech bubble: "head : tail!". Educational
textbook illustration.
[+ Universal Style Suffix]
```

#### Chapter 7 — Pattern Matching

```
A magical pointed wizard's hat with a star on it sits center-stage like a sorting hat.
Three students with name tags walk toward it: one labeled "[]", one labeled "[x]", one
labeled "[x:xs]". Each is being directed down a different corridor labeled "clause 1",
"clause 2", "clause 3". One student watches in amazement. Speech bubble from hat:
"I know which clause you need!". Hand-drawn ink sketch.
[+ Universal Style Suffix]
```

#### Chapter 8 — Recursion

```
A wise professor in bow tie and thick glasses stands next to a set of nested boxes,
each smaller than the last (like Russian dolls or nested frames). The innermost tiny
box glows with a star and says "base case = 0". The professor points at it proudly.
Speech bubble: "Trust the induction! Don't trace every call!" A confused student
watches. Educational textbook sketch.
[+ Universal Style Suffix]
```

#### Chapter 9 — Higher-Order Functions

```
A happy chef with glasses and a tall chef's hat stands at a machine labeled "map".
The chef is feeding a small scroll labeled "(*2)" into the machine as if it were an
ingredient. On the input side: a list [1, 2, 3, 4]. On the output side: [2, 4, 6, 8]
pops out. Speech bubble: "The recipe IS the ingredient!". Hand-drawn educational
illustration.
[+ Universal Style Suffix]
```

#### Chapter 10 — Lazy Evaluation

```
A programmer is peacefully sleeping in a chair. Next to them, a list "[1..]" is
unrolling infinitely across the page like a scroll rolling off a table. However, only
the first few elements that have been "taken" are awake and standing up; the rest are
asleep. A small sign says "Only computed when needed!". Whimsical educational sketch.
[+ Universal Style Suffix]
```

#### Chapter 11 — Prolog Facts & Rules

```
A friendly librarian with thick glasses uses a large rubber stamp to stamp "TRUE."
onto index cards. Each card has a Prolog fact: "likes(alice,chocolate).",
"parent(joan,peter).". A detective in a hat stands nearby asking a question with
a speech bubble: "?- happy(Who).". The librarian searches through the card files.
Educational hand-drawn illustration.
[+ Universal Style Suffix]
```

#### Chapter 12 — Unification

```
Two large puzzle pieces float toward each other in mid-air. The left piece is labeled
"foo(X, 2)". The right piece is labeled "foo(1, Y)". Between them, as they click
together, a small glowing note appears: "X=1, Y=2 ✓". Two small cartoon characters
watch from the sides, looking satisfied. Speech bubble: "They fit!". Educational
sketch style.
[+ Universal Style Suffix]
```

#### Chapter 15 — The Cut

```
A tree diagram showing branching Prolog search paths. On the main branch, a large
pair of scissors cuts off two branches labeled "X=2" and "X=3" with big X marks on
them. One green branch labeled "X=1" leads to a happy character with a checkmark.
A character watching says in a speech bubble: "Once you cut, no going back!". Bold
educational ink illustration.
[+ Universal Style Suffix]
```

#### Chapter 16 — State Problems

```
A simple board game path winding from a square labeled "START" (with a small robot
game piece) to a square labeled "GOAL". Each square along the path is labeled with a
"state(...)". Small arrow signs along the path are labeled "mov". The robot character
is mid-step, looking focused. A character on the side coaches: "Next valid move?".
Textbook sketch illustration.
[+ Universal Style Suffix]
```

#### Chapter 21 — Ten Common Mistakes

```
Split scene showing two common programmer mistakes. Left: a programmer falls into a
pit labeled "forgot the period (.)" — they look shocked, their code trailing behind
them ending without a dot. Right: a programmer is completely tangled up in a loop of
string labeled "infinite recursion — no base case!". Both characters have thick
glasses and wild hair. Educational humorous sketch.
[+ Universal Style Suffix]
```

---

## Deliverables

### Completed

| File | Description | Status |
|---|---|---|
| `prolog_translation_en.docx` | Prolog theory sections translated (pp. 76–112) | ✅ Done |
| `remaining_translation_en.docx` | Haskell theory + all practices translated (pp. 21–40, 113–148) | ✅ Done |
| `declarative_programming_complete_en.docx` | Full book in English, single document | ✅ Done |
| `declarative_for_dummies_structure.docx` | Full *For Dummies* restructure with all 22 chapters | ✅ Done |

### In Progress / Planned

| Deliverable | Description | Status |
|---|---|---|
| Chapter illustrations | 14 hand-drawn sketch images (one per major chapter) | 🎨 Brief ready |
| Final layout | Typeset version with illustrations integrated | 📋 Planned |
| Exercise solutions | Worked solutions for all new exercises | 📋 Planned |
| Spanish edition | *For Dummies* version in Spanish | 📋 Planned |

---

## How to Use This Repository

### For Authors

1. Start with `declarative_for_dummies_structure.docx` — this is the master document with the full chapter structure, all callout boxes, and new exercises.
2. Use the **illustration map** above to commission or generate one image per chapter.
3. The **predicate translation table** ensures consistent naming across all code examples.

### For Students

- If you just want to read the complete translated content, open `declarative_programming_complete_en.docx`.
- If you want the structured new edition, open `declarative_for_dummies_structure.docx`.
- The **Haskell Quick Reference** (Appendix A) and **Prolog Quick Reference** (Appendix B) are at the end of both documents.

### For Instructors

- The new exercise sets in chapters 4–16 are designed to replace the original lab sessions.
- Chapter 17 (Haskell Labs) and Chapter 18 (Prolog Labs) can be used directly as lab session handouts.
- Chapter 19 (Worked Solutions) is suitable for exam preparation sessions.

---

## Contributing

Suggestions for new exercises, improvements to explanations, or corrections to code examples are welcome. When proposing new exercises, please follow these guidelines:

- **Progressive difficulty**: exercises within a chapter go from easy to hard.
- **Real-world relevance**: prefer exercises that connect to something students recognise (text processing, simple games, familiar algorithms).
- **Both languages**: where possible, propose the same problem in both Haskell and Prolog to highlight the contrast in approach.
- **Tested**: all code examples should be verified in Hugs (Haskell) or SWI-Prolog before submission.

---

## References

### Original Book
- Carpio Cañada, J., Aranda Corral, G.A., Marco de la Rosa, J. (2021). *Programación Declarativa*. Teaching Books [95]. Universidad de Huelva.

### Illustration Inspiration
- Aulet, B. (2013). *Disciplined Entrepreneurship: 24 Steps to a Successful Startup*. Wiley. *(Illustration style reference)*

### Haskell Resources
- Lipovača, M. *Learn You a Haskell for Great Good!* — http://learnyouahaskell.com
- O'Sullivan, B., Stewart, D., Goerzen, J. *Real World Haskell* — http://book.realworldhaskell.org
- University of Pennsylvania CIS 194 course notes — https://www.seas.upenn.edu/~cis194/

### Prolog Resources
- Sterling, L., Shapiro, E. (1994). *The Art of Prolog*. MIT Press.
- Bratko, I. (1990). *Prolog Programming for Artificial Intelligence*. Addison-Wesley.
- *Ninety-Nine Prolog Problems* — https://prof.ti.bfh.ch/hew1/informatik3/prolog/p-99/
- SWI-Prolog Manual — https://www.swi-prolog.org/pldoc/
- SWISH (online Prolog) — https://swish.swi-prolog.org

### For Dummies Series
- Wiley Publishing. *For Dummies* style guidelines — https://www.dummies.com/about-for-dummies/

---

*Last updated: March 2026*
