# Plan: Typesetting Hartshorne's *Residues and Duality*

## Current State

The master document is `tex/main.tex` (book class, 12pt, built with pdflatex + biber). It
compiles to a 45-page PDF.

| Component | Status |
|---|---|
| Introduction | **Complete** |
| Chapter I, 1-2 (Triangulated categories, K(A)) | **Complete** |
| Chapter I, 3-8 (rest) | Headings only |
| Chapters II-VII | Headings only |
| Backmatter (Indices, Bibliography) | Complete |
| Appendix (Deligne) | Heading only |
| Errata | Heading only |

## OCR Sources

Two AI-OCR extractions from the original scanned PDF exist:

**doubao/** — LaTeX files, organized by chapter/section. Quality is excellent for math and
text. Covers only Chapters I-IV (parts 0-4); parts 5-10 are empty. No diagrams.

**marker/** — Markdown + LaTeX math, organized in 9 parts (~30-50 pages each). Covers the
entire book (all 7 chapters, appendix, indices, errata, 430 pages total). Quality is good
but has scattered errors (spurious bold, `h^O` for `h^0`, garbled footnotes, HTML
artifacts). Diagrams are extracted as 83 JPEG images (not LaTeX). The Deligne Appendix
pages 421-426 are severely corrupted (repeated text loop).

### Strategy for using OCR

Follow the existing conventions already established in the completed parts of `main.tex`
and the existing chapter files.

## Phases

### Phase 1: Finish Chapter I (Derived Category)

Sections 3-8 remain. **Primary source: doubao** (`part1/`). Cross-check against marker
part2 for missing content. These sections cover:

- 3: Localization of categories
- 4: Quasi-isomorphisms and the derived category
- 5: Derived functors
- 6: Ext and RHom
- 7: Way-out functors (isomorphisms between derived categories)
- 8: (if present)

### Phase 2: Chapter II (Application to Preschemes)

**Primary source: doubao** (`part2/`). Marker part2 (end) and part3 (start) for
verification. Sections:

- 1: Categories of sheaves
- 2: Derived functors of f* and Gamma
- 3: Derived functor of Hom
- 4: Derived functors of tensor and f*
- 5: Relations among derived functors
- 6: Compatibilities
- 7: Injective sheaves on a locally noetherian prescheme

### Phase 3: Chapter III (Duality for Projective Morphisms)

**Primary source: doubao** (`part3/`). Marker part3-4 for verification and diagrams.
Largest chapter. 11 sections covering differentials, f^!, trace maps, duality for
projective space, finite morphisms, the fundamental local isomorphism, the residue
symbol, and the full duality theorem for projective morphisms.

### Phase 4: Chapter IV (Local Cohomology)

**Primary source: doubao** (`part4/`). Marker part5 for verification. Main issue:
doubao uses non-standard `\motif` environments that need conversion (likely to theorem/
proposition/remark). 3 sections:

- 1: Local cohomology groups, sheaves, and complexes (Theme + 4 variations)
- 2: Depth and the Cousin complex
- 3: Generalization to complexes (Cohen-Macaulay, Gorenstein)

### Phase 5: Chapter V (Dualizing Complexes and Local Duality)

**Only source: marker** (`marker_md_part5/`, `marker_md_part6/`). Convert Markdown to
LaTeX. 10 sections:

- Introduction, example (duality for abelian groups), dualizing complexes, uniqueness,
  local cohomology on a prescheme, dualizing functors, local duality, pointwise
  dualizing complexes and f^#, Gorenstein preschemes, existence of dualizing complexes

### Phase 6: Chapter VI (Residual Complexes)

**Only source: marker** (`marker_md_part7/` start). Convert Markdown to LaTeX. 5
sections on residual complexes, functorial properties, f^! for residual complexes,
trace, and base change.

### Phase 7: Chapter VII (The Duality Theorem)

**Only source: marker** (`marker_md_part7/` end, `marker_md_part8/`). Convert Markdown
to LaTeX. 4 sections: curves over an Artin ring, the residue theorem, duality for proper
morphisms, smooth morphisms.

### Phase 8: Appendix (Deligne) and Errata

**Only source: marker** (`marker_md_part9/`). The Appendix by P. Deligne ("Cohomologie a
Support Propre et Construction du Foncteur f!") is entirely in French. Marker pages
421-426 are corrupted and will need manual reconstruction from the original scanned PDF.
The Errata page is short and well-captured in marker.

### Phase 9: Diagrams

Neither OCR source produced LaTeX for commutative diagrams. marker has them as 83 JPEG
images. Recreate them using `tikz-cd` or `\xymatrix`. The triagulated category axioms
(TR1-TR4) and octahedral diagram are the most important and appear early in Chapter I.

### Phase 10: Final pass

- Proofread all chapters against the OCR sources
- Verify cross-references between chapters
- Resolve any `??` for unresolved references
- Ensure consistent notation and formatting throughout
- Finalize bibliography entries

## Build System

Currently manual: `pdflatex` -> `biber` -> `pdflatex` x2. Consider adding a `latexmkrc`
or `Makefile` to automate. No `tikz-cd` or `xymatrix` is loaded in the preamble yet --
add when diagrams are introduced.

## Notes

- The README warns content is AI-generated and not fully proofread. Each phase should
  include checking the LaTeX output against the OCR sources.
- The existing `tex/main.tex` preamble defines all macros inline (no custom .sty files).
  Maintain this approach -- add new commands there as needed, not in separate packages.
- Doubao files each have their own preamble and `\begin{document}`. Strip these when
  merging into the chapter files. Follow the style of the already-completed sections
  in `tex/Chapter1.tex`.
- Marker uses `$$...$$` for display math. Convert to `\[...\]` per existing convention.
