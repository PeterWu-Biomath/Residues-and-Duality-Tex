---
name: OCR sources for Residues and Duality typesetting
description: Two OCR directories (doubao/ and marker/) with different strengths; always combine both
type: project
---

doubao/ has better formula/math LaTeX code but its text can be less accurate.
marker/ has more accurate text but formulas may have OCR errors.

**How to apply:** For every section being typeset, read both the doubao and marker sources side by side. Use marker as the authority for prose text, doubao as the authority for math/formula code. Neither source has LaTeX for commutative diagrams — recreate from marker's JPEG images using tikz-cd or amscd.
