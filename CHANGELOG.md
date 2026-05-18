# Changelog

All notable changes to this catalog are documented in this file.

The format follows [Keep a Changelog](https://keepachangelog.com/en/1.1.0/), and this catalog adheres to [Semantic Versioning](https://semver.org/spec/v2.0.0.html) adapted for written content: **MAJOR.MINOR** where MAJOR increments on structural reorganisations and MINOR increments on substantive content changes.

---

## [v0.9] — 2026

### README restructured around an executive-summary entrance; front-matter polish

A presentation-focused revision. The README opens with a short executive summary of content and audience instead of leading with maturity framing; Kent Beck's 3X framework now anchors the **Maturity** section rather than the introduction, and the duplicated maturity language between the two has been removed. The manuscript's front matter is tidied.

**README:**
- Entrance rewritten as a concise executive summary (content and audience), followed by a brief scope sketch; the unvalidated-engagement disclosure removed from the intro
- Kent Beck's **3X** framing relocated to lead the **Maturity** section; cross-section repetition de-duplicated
- Maturity wording clarified: patterns "not yet run against real **production** code"
- Author bio updated: 30+ years of software engineering experience alongside fifteen years of mainframe modernization

**Manuscript:**
- Dedication reworded
- Figure-plate caption alt-text removed across all plates for cleaner rendering
- PDF and EPUB regenerated

---

## [v0.8] — 2026

### Verification matures into a full part, the status-marker system retired, third thesis named

A structural revision focused on the Verification part and on how the catalog signals confidence. Part III grows from two patterns to five — gaining behavioural-specification inference, data-drift verification, and the relocated completion-criteria pattern — and the per-pattern status-marker system is retired in favour of confidence stated in prose inside each pattern body. The Preface gains a third thesis (structural vs prescriptive harness) and a third audience (AI engineers).

**Structural changes:**
- Pattern count increased from 26 to 28; all patterns from 16 onward renumbered accordingly
- New **Pattern 16: *Behavioural Specification Inference from Production Corpus*** — added to Part III (Verification)
- New **Pattern 17: *Data Drift Analysis and Verification*** — added to Part III (Verification)
- *Completion Criteria as Designed Property of Each Bounded Context* relocated from Part V into Part III as **Pattern 18**, reframed as a verification concern (the evidence a bounded context is *done*) declared during strategic recovery
- **Part III — Verification** expands from Patterns 14–15 to Patterns 14–18 — verification becomes a developed part rather than a two-pattern bridge
- **Part IV** renamed: *Governance* → ***Governance and Operating Discipline***; now Patterns 19–24
- Part V (Safe Transition and Coexistence) renumbered to Patterns 25–28
- New section after Antipatterns: **Pattern engagement across the modernization spectrum**
- Closing section restructured: *Three claims* / *What comes next* / *A word to the three audiences*

**Part structure (renumbered):**
- Part I — Strategic Recovery (Patterns 1–6)
- Part II — Tactical Generation (Patterns 7–13)
- Part III — Verification (Patterns 14–18)
- Part IV — Governance and Operating Discipline (Patterns 19–24)
- Part V — Safe Transition and Coexistence (Patterns 25–28)

**Terminology and status:**
- Subtitle updated: *"Twenty-six patterns…"* → *"Twenty-eight patterns where Domain-Driven Design meets AI-assisted blackfield mainframe modernization"*
- **Per-pattern status-marker system retired** — the *prototype-validated / in construction / designed* labels, the status-distribution sentence, and the standalone `*Status:*` lines are removed catalog-wide. Maturity is now carried in prose within each pattern body (Context, Consequences) and summarised once in the Preface's *Maturity* note, framed against Kent Beck's 3X (the catalog is in Explore). The status table is removed from the README accordingly

**Preface and front matter:**
- Added a **third thesis**: the deterministic substrates *are* the conceptual model agents work within — the distinction between *prescriptive harness* (state machines, hooks, gates) and *structural harness* (typed scaffolds, IR, ontology, tests), crediting Birgitta Böckeler's harness-engineering writing; structural harness argued to be the larger, more underestimated investment
- Added a **third audience**: *AI engineers working at the frontier of agentic coding*, alongside DDD and mainframe practitioners
- Added Chris Richardson's stance — human understanding as a *purpose*, not a fallback for AI failure
- Lineage expanded with Vlad Khononov and Pramod Sadalage; Pattern 4 develops the canonical ontology as Published Language bridging deterministic infrastructure and probabilistic agents (Evans, 2026)

**Other changes:**
- Updated all cross-references for the two new patterns, the relocation, and the renumbering
- Updated epub and pdf artifacts

**Net effect:** ~807 lines added, ~730 lines removed. Verification stops being the catalog's thinnest part; confidence moves from a label the reader filters on to an argument the reader weighs; the Preface names the harness thesis the rest of the catalog had been assuming.

---

## [v0.7] — 2026

### Strategic spectrum, the Modernization Journey, and three new patterns

The largest revision since the initial draft. The catalog gains a unifying narrative spine (*The Modernization Journey*), reframes itself around a *strategic spectrum* rather than an implicit rewrite default, retires the standalone Architectural Interlude, adds three patterns and a tenth antipattern, and closes with a new *Closing* section that states the catalog's three testable claims and its honest gaps.

**Structural changes:**
- Pattern count increased from 23 to 26; all patterns renumbered accordingly
- New **Pattern 6: *Context Map for Modernization*** — Evans' seven relationship types applied across the modernization landscape, with the distinction between *durable* and *transitional* relationships and explicit retirement criteria for the transitional ones. Status: *designed*
- New **Pattern 13: *Temporal Decoupling and Latency-Aware Data Access*** — added to Part II (Tactical Generation)
- New **Pattern 26: *Replatform with Modern Facade*** — extends the catalog to the part of the spectrum where legacy code is preserved behind a generated facade rather than rewritten. Status: *designed*
- *Transitional Architecture: The Modular Monolith as Migration Vehicle* relocated into Part V as **Pattern 22**, as the architectural vehicle the modernized side runs as during transition
- **Architectural Interlude removed** — the three-layer recovery architecture, source-provenance discipline, AsIs/ToBe ownership, and scoping note are redistributed into the patterns and the new front matter rather than living as a standalone section
- New top-level section **The Modernization Journey** (Understand / Generate / Verify / Govern / Transition / *The journey lands*) — a narrative spine that walks the five stages before the formal pattern catalog begins
- Front matter restructured: *How to read this catalog* split into **Preface**, **Who this catalog is for**, **What this catalog covers — and what it doesn't**, **What kind of patterns these are**, and **How to read it**
- New **Closing** section: *Three claims* (the catalog's three testable, falsifiable claims), *What the catalog does not yet do*, *How the catalog improves*, *A word to the three audiences*
- Added a dedication

**Part structure (renumbered):**
- Part I — Strategic Recovery (Patterns 1–6)
- Part II — Tactical Generation (Patterns 7–13)
- Part III — Verification (Patterns 14–15)
- Part IV — Governance (Patterns 16–21)
- Part V — Safe Transition and Coexistence (Patterns 22–26)

**Terminology and status:**
- Subtitle updated: *"Twenty-three patterns…"* → *"Twenty-six patterns where Domain-Driven Design meets AI-assisted blackfield mainframe modernization"*
- Status distribution updated: 15 prototype-validated, **7** in construction (was 6), **4** designed (was 2) — the new *designed* patterns are 6 and 26
- New **strategic spectrum** framing introduced up front: modernization is not a synonym for rewrite — capabilities are placed on a spectrum of rewrite / replatform / reimagine / replace with SaaS / retire, and the catalog is explicit about its rewrite-heavy centre of gravity
- **Specification-driven development (SDD)** introduced as the reimagination treatment: where the rest of the catalog treats the legacy as oracle, reimagination treats the spec as oracle (Twin Verification uncouples in this mode)

**Antipatterns:**
- Antipattern count increased from 9 to 10
- Added ***Anemic Domain Model from Agentic Translation*** — the classic Anemic Domain Model failure (Fowler, 2003) recurring with new mechanics under AI assistance, with structural correctives in Patterns 8, 9, and 19

**Other changes:**
- Updated all cross-references for the new patterns, renumbering, and removed interlude
- Updated epub and pdf artifacts

**Net effect:** ~710 lines added, ~397 lines removed. The catalog gains a narrative spine and an honest map of the modernization spectrum it serves, three patterns close real gaps (relationship design, latency-aware data access, replatform/facade), and the new Closing section makes the catalog's claims falsifiable.

---

## [v0.6] — 2026

### New part, new pattern — Safe Transition and Coexistence

Added a fifth part to the catalog and a twenty-third pattern. The catalog now answers a question it previously left open: *when is the modernization of a bounded context done?* A new Part V groups the patterns that govern the disciplined movement of a bounded context from legacy authority to modernized authority, and the dual-run period during which both sides operate.

**Structural changes:**
- Pattern count increased from 22 to 23
- New **Part V — Safe Transition and Coexistence**, between Part IV (Governance) and the Antipatterns section; the catalog is now five parts
- Patterns 21 (*Rollout and Cutover at Bounded Context Granularity*) and 22 (*Dual-Run Coexistence*) regrouped from Part IV into Part V; Part IV (Governance) is now Patterns 15–20
- New **Pattern 23: *Completion Criteria as Designed Property of Each Bounded Context*** — five-dimensional completion model (behavioural equivalence, coverage, ontological alignment, operational evidence, team-ownership transfer), calibrated per bounded context to tier and capability classification, declared during strategic recovery rather than judged at the end. Status: *designed*
- Part V opens with a numbering note: Pattern 23 is presented first, then 21 and 22, reflecting the logical order in which they apply during transition (completion gates cutover, cutover gates coexistence)
- Pattern 19 renamed: ***The Cockpit* → *The Control Plane*** — all references updated catalog-wide

**Terminology and status:**
- Subtitle updated: *"Twenty-two patterns where Domain-Driven Design meets blackfield mainframe modernization"* → *"Twenty-three patterns where Domain-Driven Design meets AI-assisted blackfield mainframe modernization"*
- Status distribution updated: 15 prototype-validated, 6 in construction, **2 designed** (was 1) — Pattern 4 and the new Pattern 23
- Reader's guide updated to four-part → five-part structure, with a note that the five parts mirror Rosetta's own stages

**Reader's guide additions:**
- Added Kent Beck's *3X framework* (Explore / Expand / Extract) to position the catalog explicitly in Explore
- Added a motivation passage (Camus epigraph) on why the catalog exists — pushing back in writing against the assumption that mainframe modernization is straightforward

**Substantive content expansions:**
- Pattern 1 (*Business-Aligned Capability Strategy*): added the facilitation discipline — the capability map's value is the shared understanding it represents, not the document; added the supporting-subdomain strategy; full Conway's Law attribution
- Pattern 2 (*The Legacy as Oracle*): added the *separation of powers* framing for the independent-oracle argument; added the *Big Ball of Mud* (Foote & Yoder) framing for ontological drift
- Pattern 3 (*The Graph as Projection*): expanded the two-epistemologies argument; distinguished deterministic graph ingestion from stable-retrieval semantics for the index; added community-detection algorithm choice (Louvain / Leiden); expanded discriminator-field and context-map explanations; added the analysis-vs-interpretation distinction
- Pattern 4 (*Domain Ontology as Independent Substrate*): expanded the substrate framing and the argument that the ontology is the most durable asset the modernization produces

**Other changes:**
- Updated all cross-references for the new pattern, part, and Pattern 19 rename
- Updated epub and pdf artifacts

**Net effect:** ~200 lines added, ~84 lines removed. The catalog gains a part and a pattern; the new material closes the completion-criteria gap and tightens several Part I patterns.

---

## [v0.5] — 2026

### Structural consolidation — twenty-two patterns, new pattern, revised architecture

Consolidated the catalog from twenty-eight patterns to twenty-two. Six patterns were merged into others or absorbed into the architectural interlude; one new pattern was added. The consolidation tightens the catalog: every remaining pattern carries more weight, cross-references are shorter, and the reader encounters less indirection.

**Structural changes:**
- Pattern count reduced from 28 to 22; all patterns renumbered accordingly
- Pattern 4 (Source Provenance Discipline) absorbed into the architectural interlude as a cross-cutting discipline rather than a standalone pattern
- Pattern 6 (The Graph and the Index as Complementary Substrates) merged into Pattern 3 (The Graph as Projection), which now covers both the structural graph and the semantic index as dual substrates
- Patterns 15 (Architecture Documentation as Pluggable Emitter), 18 (Behavioural Specifications Grown from Production), 20 (The Orchestration Layer Above Bounded Capabilities), and 26 (Spec Deltas as the Unit of Review) consolidated into neighbouring patterns
- New Pattern 20: *Team Topology and Bounded Context Alignment* — addresses Conway's Law, team ownership of bounded contexts, and the organisational counterpart to capability mapping, drawing on Skelton & Pais's team topology framework

**Terminology changes:**
- Status markers renamed: *working* → *prototype-validated*, *in progress* → *in construction*, *next* → *designed*
- Updated status distribution: 15 prototype-validated, 6 in construction, 1 designed
- Added explanatory note on what "prototype-validated" means and doesn't mean

**Antipatterns:**
- Antipattern count increased from 7 to 9
- Added *Naive self-observation* antipattern (Goodhart's Law applied to harness self-observation)
- Added *Agent army* antipattern (scaling by agent multiplication rather than harness engineering)
- Added antipatterns-and-corrective-patterns reference table

**Architectural interlude revised:**
- Restructured from per-layer sections (L1/L2/L3) to integrated narrative
- Added source provenance as cross-cutting discipline (absorbed from former Pattern 4)
- Added AsIs/ToBe ownership discipline section

**Other changes:**
- Added Matthew Skelton and Manuel Pais to the contributors list
- Added glossary entries: Conway's Law, Enabling team, Goodhart's Law
- Expanded Alignment Record concept in the cockpit pattern
- Removed visual/infographic placeholders throughout
- Updated all cross-references to reflect new pattern numbering
- Updated epub and pdf artifacts

**Net effect:** ~810 lines removed, ~750 lines added. The catalog is shorter, denser, and better organised. Every pattern that was removed is preserved in the pattern or interlude that absorbed it.

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
