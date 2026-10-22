# Template use and visual acceptance

`assets/beamer/` is a neutral adaptation of the user-selected SCU-Presentation-Beamer layout. `main.tex` is a layout specimen, not a sourced academic presentation. Replace instructional specimens with actual presentation content. Keep `PROVENANCE.md` and `LICENSE.upstream` in delivered projects. No original campus images or logos are bundled.

Use XeLaTeX or LuaLaTeX with fontspec. The font preference is TeX Gyre Heros, with automatic Arial then Latin Modern Sans fallback. Verify the selected font and Vietnamese glyphs; report any substitution. Do not introduce Chinese-font dependencies for English/Vietnamese decks.

Edit `deck-config.tex` for colors, font, language strings, and illustration paths. Empty illustration paths intentionally render without images; replace them with actual artwork for a presentation. Source figures and code diagrams belong in the output project's own assets directory.

## Compilation

Use the user's installed XeLaTeX/LuaLaTeX-compatible compiler, including Tectonic (XeTeX-based), to create a saved PDF. Check available commands and normal TeX Live/MiKTeX/Tectonic locations; a compiler installed after the shell started may not be on its current PATH. On Windows also check `%LOCALAPPDATA%/Programs/Tectonic/tectonic.exe`. Use a discovered executable by absolute path when needed. With Tectonic, run `tectonic --keep-logs main.tex` from the project directory; it handles repeated passes and downloads required TeX support files on first use. The built-in app compiler may be used when available, but its diagnostics-only tool does not export a PDF: arrange a real export or local compilation before delivery. Do not assume compilation/export success from an editor preview.

Compile the latest main.tex with the project directory as working directory and enough passes to resolve navigation, citations, and frame counts. Use noninteractive, halt-on-error options where supported. Run the bibliography stage if using BibLaTeX/Biber. Check the exit status and diagnostics. Verify that the resulting PDF exists, is nonempty, opens, contains pages, and was generated from the final sources; do not deliver a stale PDF left by an earlier successful build.

If no compatible compiler can be located, or PDF export is blocked, preserve the project and report the concrete blocker and incomplete PDF output. Never fabricate success or call source-only delivery complete. Bound repeated compiler repairs to three attempts per issue, then report the blocker.

## Visual review

Render every PDF page, including overlays, and inspect at presentation size:
- Cover/title fit; no image/text collisions or visible SCU branding.
- Text/figures remain inside the page and clear of navigation, title bars, and footer.
- Citations are present and legible; reference slides are not cramped.
- Figure labels, units, legends, and scale bars remain readable.
- Color/font/type roles are consistent; Vietnamese accents, symbols, math and bilingual terms render correctly.
- Contents, section pages, transitions, and timing match the narrative, including agenda pages and overlays.

Inspect warnings for overfull boxes and missing glyphs as well as rendered pages. Do not use global shrinking or ever-smaller fonts to hide excess content. Split or simplify without losing evidence or qualifications.

Deliver direct links to the compiled PDF and editable main.tex, plus all required supporting .tex/theme/config, figures and bibliography (also provide a source-project ZIP when useful). The PDF must already be compiled; do not leave compilation to the user. Keep audit records separate from audience-facing slides. Report independently audited scope, visual inspection coverage, and unverified items.
