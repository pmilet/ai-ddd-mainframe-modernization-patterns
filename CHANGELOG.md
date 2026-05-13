# Changelog

All notable changes to this catalog are documented in this file.

The format follows [Keep a Changelog](https://keepachangelog.com/en/1.1.0/), and this catalog adheres to [Semantic Versioning](https://semver.org/spec/v2.0.0.html) adapted for written content: **MAJOR.MINOR** where MAJOR increments on structural reorganisations and MINOR increments on substantive content changes.

---

## [v0.2] — 2026

### Structural revision — Appendix B removed, migration vocabulary integrated

Removed the standalone Appendix B (Legacy Migration Patterns reference catalog) and redistributed its content. Nick Tune's migration patterns — Bubble, Autonomous Bubble, Expose Legacy Asset, CDC vs Application-level Events, Migrate Reads First / Migrate Writes First, Republishing Legacy Events — are now defined as glossary entries and referenced inline within the patterns where they apply, rather than living in a separate appendix. This tightens the catalog: migration vocabulary appears where the reader needs it, not in a detached reference section.

**Changes:**
- Removed Appendix B (~4,500 words, 12 entries) and its associated infographic and cross-reference table placeholders
- Added glossary entries for: Asymmetrical Validation, Autonomous Bubble, Bi-directional Model Sync, Bubble, CDC vs Application-level Events, Drifting Domain Model, Expose Legacy Asset, Migrate Reads First / Migrate Writes First, Republishing Legacy Events, Tri-directional Sync
- Integrated migration-pattern references inline within Patterns 5, 12, 14, 19, 27, and 28 where the concepts are operationally relevant
- Consolidated three synchronisation antipatterns (Bi-directional Model Sync, Asymmetrical Validation, Tri-directional Sync) into a new combined antipattern entry in the antipatterns section
- Updated status count: nine patterns *in progress* → eight patterns *in progress*
- Renamed Pattern 23 to "The Harness as State Machine" (from "The Harness as Self-Observing State Machine")
- Renamed Pattern 22 to "Pattern 20 — Harness Self-Observation and Refinement"
- Updated lineage section to reference Nick Tune inline rather than through Appendix B

**Net effect:** ~270 lines removed, ~40 lines added. The catalog is shorter and more self-contained. All migration vocabulary previously in Appendix B is preserved in the glossary and in the pattern bodies where it matters.

---

## [v0.1] — 2026

### Initial draft

First public release. Twenty-eight patterns and seven antipatterns, articulated as a working catalog of AI-assisted Domain-Driven mainframe modernization practices encountered while building Project Rosetta. Approximately 41,000 words of body content.

**Status distribution:**
- 15 patterns marked *working* (validated inside the Rosetta prototype)
- 9 patterns marked *in progress* (in active construction)
- 4 patterns marked *next* (designed from validated principles but not yet built)

**Structure:**
- Part I — Strategic Recovery (Patterns 1–7)
- Part II — Tactical Generation (Patterns 8–15)
- Part III — Verification (Patterns 16–18)
- Part IV — Governance (Patterns 19–28)
- Seven antipatterns naming the failure modes the patterns are built against

**Honest disclosure:** No pattern has yet been validated against a real customer engagement. That's the next phase, not yet started. Validation to date is inside the Rosetta prototype.

**Known gaps in this draft:**
- 24 visual placeholders (figures, illustrations, code samples, tables) marked in-text but not yet rendered as production graphics
- 3 code samples sketched as descriptions but not yet implemented (Pattern 9, Pattern 11, Pattern 14)
- 2 reference tables (tier matrix in Pattern 12, antipattern reference in Antipatterns section) described but not yet rendered

These gaps will close in subsequent releases as the visual layer is produced. The textual content is review-ready as it stands.

### Available formats
- Markdown source (`AI-Assisted Domain-Driven Mainframe Modernization.md`)
- PDF (attached to this release)
- EPUB (attached to this release)

### Acknowledgements
The catalog stands on shoulders. Eric Evans, Vaughn Vernon, Martin Fowler, Sam Newman, Alberto Brandolini, Cyrille Martraire, Birgitta Böckeler, Charity Majors, Nick Tune, Kent Beck, Jeremy Miller, Anthony Alcaraz — named throughout the body where their contributions actually shaped the work.

---

## Coming next

Future releases will:
- Render the 24 visual placeholders as production graphics
- Implement the 3 code samples in C# (real Roslyn-rendered output, not pseudocode)
- Expand patterns currently below 1,000 words where review surfaces material to add
- Incorporate feedback from readers, practitioners, and the DDD/mainframe communities
- Eventually, validate patterns against real customer engagements — the milestone that converts *working* status into something stronger

The roadmap is intentionally undated. Updates happen when content is ready, not on a schedule.
