# Plan: Typesetting Hartshorne's *Residues and Duality*

## Current State

The master document is `tex/main.tex` (book class, 12pt, pdflatex + biber). Compiles to
a 45-page PDF.

| Chapter file | Book content | Status |
|---|---|---|
| `Intro.tex` | Introduction | **Complete** |
| `Chapter1.tex` | Ch I: The Derived Category | Sections 1-3 done, 4-7 are headings only |
| `Chapter2.tex` | Ch II: Application to Preschemes | Headings only |
| `Chapter3.tex` | Ch III: Duality for Projective Morphisms | Headings only |
| `Chapter4.tex` | Ch IV: Local Cohomology | Headings only |
| `Chapter5.tex` | Ch V: Dualizing Complexes and Local Duality | Headings only |
| `Chapter6.tex` | Ch VI: Residual Complexes | Headings only |
| `Chapter7.tex` | Ch VII: The Duality Theorem | Headings only |
| `Backmatter.tex` | Indices, Bibliography, Appendix (Deligne), Errata | Indices & bibliography done, appendix heading only |

## OCR Sources

Two AI-OCR extractions from the original scanned PDF:

**doubao/** — LaTeX files organized by chapter/section (`part0/` through `part10/`).
Now covers the **entire book** (all 7 chapters + appendix + indices). Each file is a
standalone `.tex` document with its own preamble. **Strong point: formula/math code.**

**marker/** — Markdown + LaTeX math (`$$...$$` / `$...$`), organized in 9 parts
(~30–50 pages each). Covers the **entire book** (430 pages). **Strong point: text
accuracy.** Diagrams are extracted as 83 JPEG images (not LaTeX).

### Key principle: always combine both sources

- **marker** has more accurate text/prose
- **doubao** has better math/formula code
- Both should be cross-referenced for every section
- Neither source produces LaTeX for commutative diagrams; recreate manually from
  marker's JPEG snapshots using `tikz-cd` or `amscd`

## Formatting Conventions

Gathered from the completed content in `tex/Intro.tex` and `tex/Chapter1.tex`:

- Display math: `\[...\]` (not `$$...$$`)
- Multi-line equations: `\begin{gathered}` inside `\[...\]`
- Theorem environments: `definition`, `proposition`, `proof` (via `amsthm`)
- Simple commutative diagrams: `\begin{CD}...\end{CD}` (via `amscd`)
- Complex diagrams: `\begin{tikzcd}...\end{tikzcd}` (via `tikz-cd`)
- Enumerate labels: `\item[a)]`, `\item[\textbf{(TR1)}]`, etc.
- Cross-references: `\cite{...}`, `\eqref{...}`, text references like `[III, 5.1]`
- No blank lines between `\chapter{...}` and first `\section{...}`
- Backmatter uses `\chapter{}` for major divisions, `longtable` for indices

Custom commands (defined in `main.tex` preamble, extend as needed):
- `\sO`, `\sF`, `\sG`, `\sL` — `\mathcal{O}`, `\mathcal{F}`, etc.
- `\DerR`, `\DerL` — double-underline `\operatorname{R}`, `\operatorname{L}`
- `\HH`, `\DD`, `\KK`, `\LL`, `\PP` — `\operatorname{H}`, `\operatorname{D}`, etc.
- `\bbP` — `\mathbb{P}`
- `\Hom`, `\Ext`, `\Tor`, `\id`, `\im`, `\Ob`, `\Spec`, `\Supp`, etc.

## Workflow per chapter

For each chapter below:
1. Copy the section structure from the existing `tex/ChapterN.tex` heading stubs
2. Read the corresponding doubao and marker files side by side
3. Write body text using marker for prose accuracy, doubao for math formulas
4. Strip standalone preambles from doubao fragments (keep only body content)
5. Recreate any commutative diagrams from marker JPEGs using `tikz-cd` / `amscd`
6. Add `\label{}` for definitions, propositions that are cross-referenced elsewhere
7. Compile and verify the PDF

## Phases

### Phase 1: Finish Chapter I (tex/Chapter1.tex)
**Sources:** doubao `part1/` + marker `part2` (pages 25-84)
- Sections 4-7 remain: Localization, Qis and derived category, Derived functors,
  Ext/RHom, Way-out functors
- Also re-check sections 1-3 against both OCR sources

### Phase 2: Chapter II (tex/Chapter2.tex)
**Sources:** doubao `part2/` + marker `part2` (end) / `part3` (start)
- Sections 1-7: Categories of sheaves, derived functors of f*, Gamma, Hom, tensor/f*,
  relations, compatibilities, injective sheaves on locally noetherian preschemes

### Phase 3: Chapter III (tex/Chapter3.tex)
**Sources:** doubao `part3/` + marker `part4`
- Sections 1-11: Differentials, f^! for smooth morphisms, cohomology calculations,
  trace map, duality for projective space, finite morphisms, fundamental local
  isomorphism, f^! for embeddable morphisms, residue symbol, trace for projective
  morphisms, duality for projective morphisms
- Largest chapter; many commutative diagrams to recreate

### Phase 4: Chapter IV (tex/Chapter4.tex)
**Sources:** doubao `part4/` + marker `part5` (pages 222-259)
- Note: doubao uses non-standard `\motif` environment — convert to standard
  theorem/remark environments
- Sections 1-3: Local cohomology groups/sheaves/complexes, depth and Cousin complex,
  generalization to complexes (Cohen-Macaulay, Gorenstein)

### Phase 5: Chapter V (tex/Chapter5.tex)
**Sources:** doubao `part5/` + marker `part5`/`part6`
- Sections 1-10: Dualizing complexes, local duality, Gorenstein preschemes, existence

### Phase 6: Chapter VI (tex/Chapter6.tex)
**Sources:** doubao `part6/` + marker `part7`
- Sections 1-5: Residual complexes, functorial properties, f^! for residual complexes,
  trace, base change

### Phase 7: Chapter VII (tex/Chapter7.tex)
**Sources:** doubao `part7/` + marker `part7`/`part8`
- Sections 1-4: Curves over Artin ring, residue theorem, duality for proper morphisms,
  smooth morphisms

### Phase 8: Appendix (Deligne) and Errata (tex/Backmatter.tex)
**Sources:** doubao `part8/`, `part9/`, `part10/` + marker `part8`/`part9`
- Appendix in French: "Cohomologie a Support Propre et Construction du Foncteur f!"
- Marker pages 421-426 are corrupted (repeated text loop) — use doubao as primary here
- Errata page is short

### Phase 9: Diagrams
- Recreate all commutative diagrams from marker's 83 JPEG images using `tikz-cd` or
  `amscd` (already loaded in preamble)
- Most important diagrams: triangulated category axioms (Ch I), octahedral axiom,
  various duality squares (Ch III, VII), proper support diagrams (Appendix)

### Phase 10: Final pass
- Proofread all chapters against both OCR sources
- Verify cross-references between chapters resolve correctly
- Ensure consistent notation throughout
- Finalize bibliography entries
- Add the Heraclitus Greek motto (marked with TODO in Intro.tex)

## Build System

Currently manual: `pdflatex` → `biber` → `pdflatex` × 2. Consider adding a `latexmkrc`.
