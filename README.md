# Residues and Duality — LaTeX edition

A typesetting and proofreading project for Robin Hartshorne’s *Residues and Duality*, including the Introduction, original Chapters I–VII, indices, bibliography, Deligne’s appendix, and the author’s errata.

**Work in progress.** Much of the initial transcription came from OCR and AI-assisted processing. Scan-comparison passes have covered the whole book, but mathematical, reference, notation, and layout checks remain incomplete. Doubao OCR can rewrite the mathematics; it must not be treated as an authoritative transcription.

## Current state

As of **27 October 2026**:

- The current source builds with installed MiKTeX and Biber to **266 pages**. Build checks find no undefined reference/citation targets, duplicate PDF destinations, missing characters, empty bibliography, or pending reference rerun.
- Scan-comparison passes cover all chapters and backmatter. All 18 printed author errata have been reconciled; retrospective review of how earlier corrections are presented is still underway.
- Subject and notation indices have linked locators. Selected destinations and notation families have been checked contextually; a resolved link does not by itself establish that the reference is correct.
- Every bibliography entry has an initial metadata investigation recorded. Some fields remain unverified; unsupported additions and erroneous name expansions have been corrected or removed.
- Visual review covers the current Introduction (PDF pages 9–18), all of original Chapters I–VII (19–238, including separating versos). Indices, bibliography, appendix, and errata (239–266) have also been reviewed; the frontmatter (1–8) remains, and some layout warnings remain open.

The editor’s built-in compiler currently fails with an auxiliary-file/font issue. The successful build evidence comes from installed MiKTeX. A clean build does not certify the original arguments or the correctness of every formula.

## Source layout

The file numbers include the Introduction, so they differ from the original book’s chapter numbers:

| Source file | Original material |
|---|---|
| `tex/main.tex` | Main document, preface, packages, and shared notation |
| `tex/chapter1.tex` | Introduction |
| `tex/chapter2.tex` | Chapter I — The Derived Category |
| `tex/chapter3.tex` | Chapter II — Application to Preschemes |
| `tex/chapter4.tex` | Chapter III — Duality for Projective Morphisms |
| `tex/chapter5.tex` | Chapter IV — Local Cohomology |
| `tex/chapter6.tex` | Chapter V — Dualizing Complexes and Local Duality |
| `tex/chapter7.tex` | Chapter VI — Residual Complexes |
| `tex/chapter8.tex` | Chapter VII — The Duality Theorem |
| `tex/Backmatter.tex` | Indices, bibliography, Deligne appendix, and errata |
| `tex/references.bib` | Main bibliography |

References retain the **original chapter and statement numbers**, not the source-file numbers. The appendix has its own local identifiers and bibliography.

Chapter filenames and includes now match exactly: `chapter1.tex` through `chapter8.tex`. A build on a case-sensitive filesystem remains to be verified.

## Editorial policy

The full convention is in [EDITORIAL_POLICY.md](EDITORIAL_POLICY.md).

- Preserve the original author’s wording, formulas, statements, and arguments in the body, including errors in the original printing.
- Put corrections, qualifications, counterexamples, and supplied proof steps in clearly labelled footnotes. If the discussion exceeds one typeset page, use a separate editorial remark section with a pointer footnote.
- Label the author’s printed errata separately from new editorial corrections.
- Repair OCR/transcription errors against the scans. An OCR invention is not original text to preserve. Git history helps recover edits, but scans establish what was printed.
- Preserve historical bibliography wording and distinguish it from added metadata. Verify or remove unsupported enrichment.

Notation is modernized while retaining the original distinctions:

| Meaning | Source macro |
|---|---|
| Ordinary Hom group or module | `\Hom` |
| Sheaf Hom in script font | `\sheafHom` |
| Global derived Hom | `\RHom` |
| Derived sheaf Hom | `\RsheafHom` |
| Sheaf Ext / Tor | `\sheafExt`, `\sheafTor` |
| Derived functors / tensor product | `\RR`, `\LL`, `\derivedtensor` |

A superscript bullet can denote an actual Hom complex; do not mechanically replace every Hom complex by derived Hom. The notation index explains the convention replacing the original single/double underlines.

## Build

Use a LaTeX installation with pdfLaTeX, Biber, and the packages loaded by `tex/main.tex` (including BibLaTeX, TikZ-CD, New PX, and Mathrsfs). From the repository root:

```sh
cd tex
pdflatex -interaction=nonstopmode -halt-on-error main.tex
biber main
pdflatex -interaction=nonstopmode -halt-on-error main.tex
pdflatex -interaction=nonstopmode -halt-on-error main.tex
```

The output is `tex/main.pdf`. Check the final log for unresolved references, rerun requests, missing glyphs, and layout warnings, then inspect the rendered pages. Generated PDFs and most auxiliary files are not tracked.

## Remaining work

The next visual pass starts at **the frontmatter**, `tex/main.tex`, PDF page **1** in the current build. Page numbers here refer to the generated PDF, not the original scan. Review the rendered pages, repair confirmed layout problems, rebuild after source changes, and record the exact pages checked. Continue the reference, notation, and preservation audits alongside this pass.

- [ ] **Finish the original-text preservation review.** Classify earlier inline changes against Git history and scans; move remaining author corrections and editorial supplements into the required notes/remarks.
- [ ] **Complete the semantic reference audit.** Check every statement/equation locator, visible original number, citation postnote, appendix-local reference, and PDF destination against the intended passage.
- [ ] **Complete the contextual notation audit.** Check Hom/sheaf Hom/RHom/derived sheaf Hom, ordinary versus derived tensor, global versus sheaf cohomology, and global versus internal duality throughout the text.
- [ ] **Resolve or document the remaining mathematical checkpoints.** Review fixed-filtration uses of VI Proposition 1.1(c) in VI–VII variance/trace constructions, the residual-complex uniqueness exercise, and the appendix’s conditional independence/associativity/compatibility, truncation, and formal pro/Ind duality calculations. Preserve explicitly omitted proofs as such; do not present source repair as proof completion.
- [ ] **Finish checking added bibliography metadata.** All 31 entries have been investigated initially, but partial records and access failures leave open fields. Verify those fields against reliable original-edition evidence or remove unsupported additions, without replacing historical citations with later editions.
- [ ] **Review every page of the current PDF.** Check formulas, diagrams, footnote continuations and length, headings, table breaks, indices, bookmarks, and links. Recheck affected pages after edits or pagination changes.
- [x] **Normalize filename/include capitalization:** all eight chapter filenames match their lowercase includes.
- [ ] **Run the final completion audit.** Rebuild with Biber as needed, converge references, refresh inventories, and record evidence for each closed item. The book is not ready to declare fully proofread.

