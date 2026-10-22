---
name: source-to-latex-slides
description: Create source-grounded English or Vietnamese LaTeX Beamer presentations from provided papers, PDFs, notes, or links, with academic citations, concise storytelling, source figures or code-drawn diagrams, independent citation review, and visual verification. Not for PowerPoint-only requests.
---

# Source to LaTeX slides

Create concise, clear, lively, coherent academic slides. Use the supplied SCU-derived layout without SCU logos or institutional text. Adapt colors and illustrative imagery to each presentation; do not redesign the layout unless requested.

## Establish the brief

Reuse answers already provided. Ask for missing essentials together:
- Slide language: explicitly offer English or Vietnamese; never silently assume one.
- Audience, prior knowledge, presentation goal, emphasis and exclusions.
- Duration, and whether questions are included.
- Provided sources and which are mandatory.

Keep technical terms in their original language. In Vietnamese slides, pair an accurate Vietnamese translation with the original term at first use when useful; do not force misleading translations. Use terminology consistently. Explain difficult ideas with examples understandable to a high-school student while preserving scientific precision and the requested audience depth.

Use only provided sources for substantive content. Ask before expanding the source set. Retrieve provided links and inspect originals, not just search snippets. If a source is inaccessible, report the gap and request an accessible copy or omit unsupported material.

## Ground the narrative

Read [references/evidence-review.md](references/evidence-review.md). Inventory sources and map proposed claims, equations, numbers, examples, figures, and diagrams to precise source locations. A bibliography entry is not proof of a claim.

Choose a deductive, inductive, or mixed narrative:
- Deductive: main message, explanation, evidence.
- Inductive: problem or evidence, analysis, conclusion.
- Mixed: choose per section with clear transitions connecting sections.

Propose slide count and pacing from duration and complexity, including section dividers and overlays. Give each content slide one main message. Use concise text, meaningful visuals, and explicit connections between slides. Preserve limitations, uncertainty, attribution, and distinctions between correlation and causation. Never simplify into a false claim.

Before building the full deck, show the outline with narrative choice and timing, plus a rendered cover and representative content slide for approval. Continue if already approved or the user explicitly requests an uninterrupted build. Silence is not approval.

## Build from the template

Read [references/template-and-qa.md](references/template-and-qa.md). Copy `assets/beamer/` into a dedicated presentation project, retaining license and provenance. Edit that copy, not the installed skill; `main.tex` is the entrypoint.

Preserve the cover composition, colored title bars, section navigation, section dividers, three-part footer, and image-led contents/closing layouts. Remove SCU logos, campus images, Chinese sample text, and institutional branding from visible slides. Show presenter and institution only if supplied. Keep attribution in project files, not as slide branding.

Use 16:9 by default and a consistent font supporting English and Vietnamese diacritics. Choose a coherent topic-specific palette and a distinct thematic cover illustration per deck. Set them in `deck-config.tex`. Maintain readable contrast and consistent type roles throughout.

Visual rules:
- Prefer relevant figures extracted directly from provided sources. Cite source and figure/page. Crop margins or resize without changing meaning; preserve labels, legends, scale bars, and units.
- Never generate or reconstruct scientific evidence images, experimental results, or data plots with ImageGen.
- Redraw charts from original provided data when beneficial. Preserve values, units, scales, uncertainty, and provenance; disclose transformations. Do not estimate missing data from appearance and present it as original data.
- Draw flowcharts, mechanisms, conceptual diagrams, and structured schematics with code, preferably TikZ. Charts may use PGFPlots or an available plotting tool. Cite the sources supporting their content.
- Use the available imagegen skill/tool only for non-evidentiary thematic illustrations, such as cover or section imagery. Label them as illustrative where confusion with evidence is possible. Never pass extracted research figures through ImageGen.

Use numeric short citations on slides and full references at the end unless requested otherwise. Reserve room for citations in each slide's content area. Structural titles, navigation, author metadata, and decorative elements do not need scientific citations. All substantive knowledge does, including in titles and captions.

## Independently review evidence

Call an independent review agent with the actual sources, finished slide content, figures/data, source inventory, and evidence map. This required citation audit does not authorize delegation of unrelated work. Follow the audit contract in `references/evidence-review.md`.

Resolve material mismatches and unsupported claims, then send changed content for re-review. If independent agents are unavailable, disclose that the required audit remains incomplete; self-review is not a substitute. Do not call the deck fully verified until this requirement is met.

## Verify and deliver

Compile the final .tex sources into an actual saved PDF file, inspect diagnostics, and render every page. Use the user's installed compatible compiler; detect it rather than assuming it is unavailable because the current shell has a stale PATH. A successful compilation diagnostic or an editor preview without an exported PDF is not a deliverable. Confirm the PDF exists, opens, has pages, and reflects the latest sources. Visually inspect every slide and overlay for clipping, overlaps, unreadable figures/citations, inconsistent fonts, and Vietnamese glyph errors. Inspect both English and Vietnamese specimens when changing the reusable template. Fix problems and recheck changed pages. Compilation alone is not visual verification.

Prefer reducing content or splitting slides over shrinking text. Keep all visible elements inside the page and content clear of navigation, title, and footer. Recheck pacing after revisions.

The required outputs are (1) the final compiled .pdf and (2) editable .tex source files. Link directly to both in the final response; do not substitute pasted LaTeX, an editor tab, or instructions telling the user to compile it themselves. Include theme/config, figures, bibliography, and figure-generation code needed to rebuild the PDF, preferably also as a source-project ZIP. Include the evidence map and review results as project-side records, with a concise check report. If compilation or PDF export is genuinely blocked, preserve sources, report the concrete blocker, and mark the requested output incomplete. Do not publish or upload externally unless requested.
