# UL 508A MTR exam study site

**Live site:** https://deg333.github.io/ul-practice/ (GitHub Pages, served from the `main` branch root).

Or open **`index.html`** in a browser (works offline, no build step; `ul508a-mtr-study.html` just redirects to it). Keep the `vendor/katex/` folder next to it: it holds [KaTeX](https://katex.org) (MIT, v0.16.11) used to typeset the math. Without it the page falls back to loading KaTeX from a CDN, or shows the formulas as plain text when offline.

- **Interactive tables** – hover highlights the row and column (merged headers handled), click pins the highlight and copies the value (numbers copied without commas/units), Esc clears
- **Bookmark tabs** (left edge) – five colored tabs that slide out reference tables from any page: Motor FLC, Protection & rounding, Wire (Tables 28.1 / 38.1), SCCR (SB4.1 / SB4.2) and Transformers (450.3(B), SB4.3 / SB4.4)
- **Scratch pad sidebar** (📝 button, top right) – graph-paper *Given / Find / Equations / Solution* worksheet: define variables with subscripts (`V_L`, `I_ph`), write equations that use them, and get typeset steps (formula → numbers substituted → result) with the Find answers boxed; works alongside the calculator
- **Calculator sidebar** (🖩 button, top right) – expression calculator with variables (`kva = 75`), `ans`, `%`, `sqrt`, trig in degrees, the power formulas for DC / single-phase / 3-phase circuits (`dc_vi`, `ac1_vi`, `ac3_l` …) and exam helpers (`up`/`down` standard sizes, `i3`, `isc3`, `flc3`, `wire`)
- **Exam Parts** – questions organised like the exam: Part 1 General UL 508A Information, Part 2 Enclosed Panels and Power Circuits, Part 3 Control Circuits / Ratings / Markings / Enclosures, Part 4 SCCR – each with study notes, practice and a quiz
- **FLC vs nameplate, Table 28.1 and Table 38.1** – the NEC 430.6(A) rule as a graphic with a worked 40 hp nameplate example, UL 508A conductor ampacities (copper and aluminum) and control-circuit conductor sizes, with practice questions
- **Eaton SCCR slide notes** – steps to determine panel SCCR, field-supplied current-limiting feeder devices (SB4.3.4 + example label), current-limiting fuse and breaker scenarios (redrawn as SVG) and the power-transformer example, with 8 practice questions
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

## Part 3 sourced from the Siemens manual
Part 3 notes and questions were rewritten from the Siemens reference manual (08/2014): Class 1 / Class 2 / low-voltage limited energy limits (Table 7-1), control circuit protection (Tables 41.1, 41.2, 42.1, 42.2), circuit grouping and separation, wire colour and sizing, nameplate, field-wiring terminal markings, warning labels and device markings. Each question cites the manual's chapter and page. Items that disagree with the Eaton guide (Table 41 values; 500 % vs 300 % for CPT primary < 2 A) are flagged in the text. The manual is from 2014, so confirm against the edition your exam uses.

## 3-Phase Phasors page
New **3-Phase Phasors** tab with six animated, interactive diagrams (from PDH Online E431, “The Square Root of Three in Electrical Calculations”): rotating phasors and sine waves; V<sub>L-L</sub> = √3 V<sub>L-N</sub> built by vector subtraction; delta line currents (balanced vs unbalanced, with a power-factor slider); wye neutral current as a tip-to-tail vector sum; closed vs open delta banks; and why the voltage-drop formula has √3. Six matching practice questions (ph-1 to ph-6) are in the question bank.

## Control transformer protection corrected to UL 508A Tables 42.1 / 42.2
Control-transformer items (questions, lessons, simulator) now use UL 508A Table 42.1 (primary only: ≥ 9 A 125 %, 2–8.99 A 167 %, < 2 A 500 %) and Table 42.2 (primary + secondary: primary 250 %, or 500 % below 2 A; secondary 125 % / 167 %). Power transformers keep NEC 450.3(B) (300 % below 2 A). The simulator has a transformer-type selector.

## Heater service problem tab
The 3-Phase Phasors page now has two tabs. "Problem: heater service" works the 230 V, 3-phase unbalanced heater example (editable counts and watts): leg and line currents by vector difference, maximum demand, 125 percent continuous sizing, feeder and branch circuit breakers, an animated phasor construction, and a one-line diagram. Questions ph-7 and ph-8 match it.

## Typeset, editable scratch pad
Given, Find and Equations are now shown as KaTeX-typeset math. Click (or tab into) any line to edit the plain text, and click away to see it typeset again; invalid lines show as red text with the error on hover.

## Heater problem: add groups, wye version
The heater problem now lets you add and remove heater groups on every leg, and a new tab solves the same kind of problem on a wye (4-wire) service with line-to-line and line-to-neutral groups, neutral current, 1-pole and 2-pole breakers and a one-line diagram.

## SCCR Practice page
A new **SCCR Practice** tab generates random, realistic 480 V panels (3-9 branch circuits: motor, heater, control; feeder with fusible disconnect or main breaker). Pick or type each branch SCCR and interrupting rating, the feeder values and the final panel SCCR, then check, retry or show the step-by-step solution. Easy/Medium/Hard levels (Hard adds invalid tested-combination traps), numbered problems and a score. Laid out for desktop and iPhone 15 width.
