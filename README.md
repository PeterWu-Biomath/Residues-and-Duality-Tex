# Residues and Duality — LaTeX edition

A typesetting and proofreading project for Robin Hartshorne’s *Residues and Duality*, including the Introduction, original Chapters I–VII, indices, bibliography, Deligne’s appendix, and the author’s errata.

**Book-wide typesetting/proofreading pass completed.** Much of the initial transcription came from OCR and AI-assisted processing. Scan-comparison, reference, notation, preservation and final verification passes cover the whole book. Doubao OCR can rewrite the mathematics; it must not be treated as an authoritative transcription.

## Current state

As of **15 November 2026**:

- The current source builds with installed MiKTeX and Biber to **284 pages**. Build checks find no undefined reference/citation targets, duplicate PDF destinations, missing characters, empty bibliography, or pending reference rerun.
- A complete English translation follows Deligne’s French appendix, before the errata. All five sections, formulas, diagrams, bibliography and 14 footnotes are included. Scan-confirmed omissions are restored in both versions.
- Scan-comparison passes cover all chapters and backmatter. All 18 printed author errata have been reconciled; identified earlier corrections have been reconciled with the preservation policy.
- All explicit internal references, including index links, have been checked in context. A pass over numbered plain-text references added 31 links without changing the wording. Bibliography page links lead to the correct printed folios. External citations retain their recorded edition caveats; six unavailable locators remain as printed, as requested.
- Hom and Ext/Tor notation has received a contextual pass throughout the chapters and appendix; cohomology notation has also been checked in IV–VII, and tensor notation in VI–VII. The final notation/duality consistency check is complete.
- Added metadata in all 31 bibliography entries has been reviewed; unsupported additions were removed. Historical-edition and citation caveats remain.
- All pages of the current **284-page PDF** have visual coverage: changed pages were inspected and the others match reviewed images. No overfull boxes remain. These checks do not certify every original proof.

Build verification uses installed MiKTeX. The edition retains original mathematical errors and provisional arguments with labelled notes; a clean build does not certify the original proofs.

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
pdflatex -synctex=1 -interaction=nonstopmode "main.tex"
biber main
pdflatex -synctex=1 -interaction=nonstopmode "main.tex"
pdflatex -synctex=1 -interaction=nonstopmode "main.tex"
```

The output is `tex/main.pdf`. Check the final log for unresolved references, rerun requests, missing glyphs, and layout warnings, then inspect the rendered pages. Generated PDFs and most auxiliary files are not tracked.

## Review status

No required tasks remain from this pass. Original provisional arguments and documented historical citation limits are retained.

- [x] **Review original-text preservation.** Reconciled identified corrections with scans and earlier patches; original errors remain in the body with labelled corrections or remarks.
- [x] **Retain the original citations.** Accessible citation checks and edition caveats are recorded. The six locators whose source pages were unavailable are retained as printed, as requested; they are not marked verified.
- [x] **Complete the contextual notation audit.** Hom, Ext/Tor, tensor and cohomology symbols have book-wide contextual coverage; definitions, notation index and global/sheaf duality conventions agree.
- [x] **Document the mathematical qualifications.** VI–VII's common filtrations and the appendix's compactification, truncation and formal pro/Ind issues are documented in editorial notes. Original exercises, conditional arguments and omitted compatibility proofs remain identified as such.
- [x] **Check added bibliography metadata.** Reviewed the current fields in all 31 entries against scans and primary/institutional records; removed unsupported additions. Historical citations and exact-edition caveats are retained.
- [x] **Finish the current layout pass.** All 284 pages are covered; no overfull boxes remain. Split statements, long headings/formulas and blank-verso headers have been addressed.
- [x] **Normalize filename/include capitalization:** all eight chapter filenames match their lowercase includes.
- [x] **Run the final completion audit.** Current source/PDF hashes, all 284 reviewed pages, 953 reference commands, 109 bibliography page links and 31 printed cited-on lists pass verification.

