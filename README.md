# Residues and Duality — LaTeX edition

A typesetting and proofreading project for Robin Hartshorne’s *Residues and Duality*, including the Introduction, original Chapters I–VII, indices, bibliography, Deligne’s appendix, and the author’s errata.

**Work in progress.** Much of the initial transcription came from OCR and AI-assisted processing. Scan-comparison passes have covered the whole book, but mathematical, reference, notation, and layout checks remain incomplete. Doubao OCR can rewrite the mathematics; it must not be treated as an authoritative transcription.

## Current state

As of **13 November 2026**:

- The current source builds with installed MiKTeX and Biber to **284 pages**. Build checks find no undefined reference/citation targets, duplicate PDF destinations, missing characters, empty bibliography, or pending reference rerun.
- A complete English translation follows Deligne’s French appendix, before the errata. All five sections, formulas, diagrams, bibliography and 14 footnotes are included; the French text is unchanged.
- Scan-comparison passes cover all chapters and backmatter. All 18 printed author errata have been reconciled; retrospective review of how earlier corrections are presented is still underway.
- All explicit internal references, including index links, have been checked in context. A pass over numbered plain-text references added 31 links without changing the wording. Bibliography page links lead to the correct printed folios. External citation details still need checking.
- Hom and Ext/Tor notation has received a contextual pass throughout the chapters and appendix; cohomology notation has also been checked in IV–VII, and tensor notation in VI–VII. Other notation checks remain open.
- Added metadata in all 31 bibliography entries has been reviewed; unsupported additions were removed. Historical-edition and citation caveats remain.
- The earlier 266-page layout received a full visual pass. All pages of the English translation have now been inspected; the remaining book-wide layout changes still need a final review. Small layout warnings remain. These checks do not certify every original proof.

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
| `tex/appendix-english.tex` | English translation, included after the French appendix |
| `tex/references.bib` | Main bibliography |

References retain the **original chapter and statement numbers**, not the source-file numbers. The appendix has its own local identifiers and bibliography.

Chapter filenames and includes now match exactly: `chapter1.tex` through `chapter8.tex`.

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

The full visual pass is complete. Continue the reference, notation and original-text preservation checks, and recheck affected pages after edits.

- [ ] **Finish the original-text preservation review.** Identified corrections now have review records across all chapters and backmatter. Reconcile their coverage with the earlier change history and check that every added correction is in a labelled note or remark.
- [ ] **Finish checking citation details.** Explicit internal links and numbered plain-text locators have received a pass. Check external citation postnotes and review remaining free-form locators during the preservation pass.
- [ ] **Complete the contextual notation audit.** Hom, Ext/Tor, tensor and cohomology symbols have received contextual passes across the book. Finish the final notation and duality consistency review.
- [x] **Document the mathematical qualifications.** VI–VII's common filtrations and the appendix's compactification, truncation and formal pro/Ind issues are documented in editorial notes. Original exercises, conditional arguments and omitted compatibility proofs remain identified as such.
- [x] **Check added bibliography metadata.** Reviewed the current fields in all 31 entries against scans and primary/institutional records; removed unsupported additions. Historical citations and exact-edition caveats are retained.
- [x] **Complete the first visual pass of all 266 PDF pages.**
- [ ] **Finish layout polish.** Address sparse chapter endings and remaining overfull warnings. The split definition and separating-verso headers have been repaired. Recheck affected pages after edits.
- [x] **Normalize filename/include capitalization:** all eight chapter filenames match their lowercase includes.
- [ ] **Run the final completion audit.** Rebuild with Biber as needed, converge references, refresh inventories, and record evidence for each closed item. The book is not ready to declare fully proofread.

