# Changelog

All notable changes to this catalog are documented in this file.

The format follows [Keep a Changelog](https://keepachangelog.com/en/1.1.0/), and this catalog adheres to [Semantic Versioning](https://semver.org/spec/v2.0.0.html) adapted for written content: **MAJOR.MINOR** where MAJOR increments on structural reorganisations and MINOR increments on substantive content changes.

---

## [v0.4] — 2026

### Architectural Interlude added

Added a new section between Part I and Part II: *Architectural Interlude — The Three-Layer Recovery Architecture (CICS Instantiation)*. This makes explicit the three-layer discipline (L1 Syntactic/Resource Graph, L2 Semantic Intent Graph, L3 Architectural Target Graph) that the catalog has been articulating implicitly across its patterns, including the architect-gated transitions between layers.

**Changes:**
- Added ~70-line architectural interlude section between Part I and Part II
- Added introductory paragraph in the reader's guide noting the interlude and its placement
- L1 (evidence, not interpretation), L2 (specification the original team never produced), L3 (architectural target) described with pattern cross-references
- Architect-gated transitions documented: L1→L2 via heuristic catalog, L2→L3 via mapping rules, L3→scaffold via scaffold-meta.json
- Properties table: verifiable, reviewable, governable, constitutional
- Scoping note clarifying CICS instantiation and substrate-independence question
- Updated epub and pdf artifacts

---

## [v0.3.1] — 2026

### Housekeeping — README and repository hygiene

Updated README to reflect the v0.3 release and improved repository setup.

**Changes:**
- Updated status badge from `draft v0.1` to `draft v0.3`
- Updated PDF and EPUB download links to point to v0.3 release assets on GitHub
- Added Uberto Barbini to the contributors list in the README
- Added `.gitignore` to exclude `.claude/` directory from version control

---

## [v0.3] — 2026

### Uberto Barbini's contributions integrated

Integrated Uberto Barbini's work on agent execution discipline and failure modes into the catalog. Three areas of contribution: the *one prompt, one commit* principle as a unit-of-change discipline for agent-produced work, the taxonomy of agent execution failure modes (*loop of death*, *misunderstanding the requirement*, *desperate changes*) with detection and corrective mechanisms at platform scale, and the idea of deriving heuristic catalog entries from operational history (git history and PR comments as input to agent rules).

**Changes:**
- Pattern 22 (Heuristics as Explicit Artifacts): added paragraph on deriving catalog entries from operational history, referencing Barbini's experiments with generating rule files from git history and PR comments
- Pattern 23 (The Harness as Self-Observing State Machine): added paragraph on *one prompt, one commit* principle as unit-of-change discipline; added paragraph on agent execution failure modes with platform-scale detection mechanisms (cycle detection, scaffold-boundary violation, invariant violation)
- Glossary: added *Agent execution failure modes* entry defining loop of death, misunderstanding the requirement, and desperate changes, with cross-references to Patterns 22 and 23
- Added Uberto Barbini to the contributors list in the introduction and lineage section
- Updated epub and pdf artifacts

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
The catalog stands on shoulders. Eric Evans, Vaughn Vernon, Martin Fowler, Sam Newman, Alberto Brandolini, Cyrille Martraire, Birgitta Böckeler, Charity Majors, Nick Tune, Uberto Barbini, Kent Beck, Jeremy Miller, Anthony Alcaraz — named throughout the body where their contributions actually shaped the work.

---

## Coming next

Future releases will:
- Render the 24 visual placeholders as production graphics
- Implement the 3 code samples in C# (real Roslyn-rendered output, not pseudocode)
- Expand patterns currently below 1,000 words where review surfaces material to add
- Incorporate feedback from readers, practitioners, and the DDD/mainframe communities
- Eventually, validate patterns against real customer engagements — the milestone that converts *working* status into something stronger

The roadmap is intentionally undated. Updates happen when content is ready, not on a schedule.
