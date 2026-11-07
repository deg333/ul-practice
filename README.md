# UL 508A MTR exam study site

Open **`ul508a-mtr-study.html`** in a browser (works offline, no build step). Keep the `vendor/katex/` folder next to it: it holds [KaTeX](https://katex.org) (MIT, v0.16.11) used to typeset the math. Without it the page still works and shows the formulas as plain text.

- **Interactive tables** – hover highlights the row and column (merged headers handled), click pins the highlight and copies the value (numbers copied without commas/units), Esc clears
- **Bookmark tabs** (left edge) – five colored tabs that slide out reference tables from any page: Motor FLC, Protection & rounding, Wire (Tables 28.1 / 38.1), SCCR (SB4.1 / SB4.2) and Transformers (450.3(B), SB4.3 / SB4.4)
- **Calculator sidebar** (🖩 button, top right) – expression calculator with variables (`kva = 75`), `ans`, `%`, `sqrt`, trig in degrees and exam helpers (`up`/`down` standard sizes, `i3`, `isc3`, `flc3`, `wire`)
- **Exam Parts** – questions organised like the exam: Part 1 General UL 508A Information, Part 2 Enclosed Panels and Power Circuits, Part 3 Control Circuits / Ratings / Markings / Enclosures, Part 4 SCCR – each with study notes, practice and a quiz
- **FLC vs nameplate, Table 28.1 and Table 38.1** – the NEC 430.6(A) rule as a graphic with a worked 40 hp nameplate example, UL 508A conductor ampacities (copper and aluminum) and control-circuit conductor sizes, with practice questions
- **Supplement SB tables** – SB4.1 (default SCCR), SB4.2 (fuse let-through, both pages), SB4.3 / SB4.4 (transformer secondary short-circuit current) on the Reference tab, a *Let-through lookup* simulator, and practice questions
- **SCCR worksheets** – the seven panel/branch worksheets redrawn as SVG schematics with multiple-choice answers and full branch-by-branch evaluation, plus notes on the current-limiting-device / transformer evaluation method (Tables SB4.2 / SB4.3)
- **Three dedicated practice sections** – *Power Transformers*, *Control Transformers* and *SCCR* – each with a step-by-step lesson, then practice questions with hidden answers and full math (plus a quiz-this-section button)
- Study questions with hidden answers, worked math steps and explanations (numeric answer checker)
- Quiz mode with progress tracking (saved in the browser)
- Reference tables (motor FLC, protection percentages, conductor ampacity, default SCCR, formulas)
- Simulators: SCCR weakest-link builder, motor branch-circuit calculator, animated start/stop ladder with thermal-overload trip curve, 3-phase waveforms/phasors/power triangle, transformer protection and fault-current calculators

Table values and percentages are study aids – verify against the edition of UL 508A / NEC your exam uses.
Topics are cross-checked against the Eaton *Control panel design guide (UL 508A)* and transformer-current articles from Larson Electronics and Industrial Monitor Direct.

Math: formulas written as plain text inside `<code>` elements are converted to LaTeX at runtime (fractions, subscripts, units) and rendered with KaTeX; anything the converter can't parse is left as plain text.
