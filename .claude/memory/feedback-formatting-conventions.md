---
name: Formatting conventions for the book
description: LaTeX conventions established in Intro.tex and Chapter1.tex; follow these for all new content
type: feedback
---

Use `\[...\]` for display math (not `$$...$$`). Use `\begin{CD}...\end{CD}` for simple commutative diagrams, `\begin{tikzcd}...\end{tikzcd}` for complex ones. Multi-line equations use `\begin{gathered}`. Theorem environments: `definition`, `proposition`, `proof`. No blank line between `\chapter{...}` and first `\section{...}`.

**Why:** These conventions are already established in the completed parts of the book.

**How to apply:** When writing new chapter content, copy the style of tex/Chapter1.tex. Strip standalone preambles from doubao fragments — keep only body content. Use macros defined in main.tex preamble (e.g., `\sO`, `\DerR`, `\HH`, `\DD`, `\Hom`, `\Ext`).
