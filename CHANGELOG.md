# Changelog

All notable changes to this catalog are documented in this file.

The format follows [Keep a Changelog](https://keepachangelog.com/en/1.1.0/), and this catalog adheres to [Semantic Versioning](https://semver.org/spec/v2.0.0.html) adapted for written content: **MAJOR.MINOR** where MAJOR increments on structural reorganisations and MINOR increments on substantive content changes.

---

## [v1.0.17] — 2026

### Epistemic honesty pass across Parts III–IV: Witness marked as designed-not-built, candidate vs. full patterns named, and the verification cluster's expert-advisor discipline made explicit

A cross-cutting revision that sharpens what the catalog claims and how confidently. Three threads run through it. First, an *epistemic-status* pass: the Preface now distinguishes patterns that have recurred in the building (Rosetta-exercised) from *candidate patterns* reasoned forward from principle, and reframes a pattern's concreteness as a signal of how far its learning has travelled. Second, **Witness** — the production-mode verification layer — is consistently reframed as *designed but not yet built* wherever the prose had drifted into present-tense "it verifies / it owns." Third, the Part III verification patterns gain an explicit articulation of the *measurement-is-deterministic, interpretation-is-advisory* split the rest of the catalog already turns on, plus a sweep of pattern cross-reference renumbering corrections.

**Manuscript:**
- **Preface** — two new framing paragraphs: *not every pattern has earned the name* (Rosetta-exercised patterns vs. candidate patterns awaiting field confirmation, with the Consequences section read as the status marker); and *concreteness as signal* — abstract patterns mean "the principle is known, the specifics are still emerging," not a chapter left thin
- **Witness reframed as planned throughout** — Pattern 2's pipeline note, Pattern 14, Pattern 15 ("designed as the production-mode counterpart… not yet built"), Pattern 19's four-server description, Pattern 26 (parallel-run / reconciliation), and the appendix all now say Witness is *designed*/*intended*, not running
- **Pattern 4 (*Domain Ontology as Independent Substrate*)** — Gruber's (1993) formal definition of *ontology* added (a formal, explicit specification of a shared conceptualisation); new *ontology IS code* framing after Tony Seale (2026) — the ontology is machine-checkable (satisfiability, entailment tests, contradiction-as-failed-build) and governed through the harness (Pattern 22), which can gate a change that fails its checks
- **Part III opener** — rewritten to name verification's *four axes* and its **boundary**: verification establishes what is *true* of the running system, not what it *ought* to become (descriptive vs. normative); and the cluster-wide *measurement deterministic / interpretation advisory* discipline stated up front
- **Pattern 16 (*Behavioural Specification Inference*)** — a full **worked example** (a savings-account overdraft-fee signature carried through all four stages into a domain-language Given-When-Then); the **descriptive-vs-normative** distinction (a captured behaviour the business may want to *retire*, routed to Pattern 1 rather than silently encoded); and a **silent-coverage-risk** paragraph (an inferred suite is a floor, not a ceiling — corpus coverage must be measured, not assumed)
- **Pattern 17 (*Data Drift Analysis*)** — new *measurement-deterministic, interpretation-advisory* paragraph (agents triage drift against the Pattern 15 taxonomy, propose per-field epsilons, read temporal discrepancies; humans ratify); and a **remediation-per-category** paragraph (each drift class implies its own correction, and the cost rises with how long it ran undetected — the economic argument for snapshot cadence)
- **Pattern 18 (*Completion Criteria*)** — reframed from *"is it done?"* to *"is it good enough to hand off?"*: a living architecture is never finished, perfection is asymptotic, so the six dimensions become *quality indicators measured against declared thresholds*, not pass/fail facts; operational evidence requires a **full business cycle** (month-end, quarter close, year-end), not a fixed window; new agent-as-advisor paragraph
- **Pattern 21 (*Heuristics as Explicit Artifacts*)** — conditions of application written in the **ontology's vocabulary** (Pattern 4), coupling the two substrates; an open design question on the **shape** of a heuristic — a deterministic *envelope* wrapping a probabilistic *core* (a versioned prompt fragment) where the judgement cannot reduce to weights; the heuristic schema named as a **published language**
- **Pattern 19** — Evans *Domain Navigator* citation tightened (domainlanguage.com, January 2026); **Pattern 22** — eval-suite-gap discussion tightened, "architectural commitment" wording
- Pattern cross-reference **renumbering corrections** throughout (e.g. 25→22, 26→24, 19→16, 20→17) and several heading-level fixes (`###` → `####`)
- PDF and EPUB regenerated

**README:**
- Status badge bumped from `v1.0.16` to `v1.0.17`
- PDF and EPUB download links point to the `v1.0.17` release

**Net effect:** ~+65/−35 lines in the manuscript, spread across the Preface, Pattern 4, the Part III opener, and Patterns 16–22 rather than concentrated in one pattern. Pattern count remains 28; no new patterns, no structural change. The revision lowers the catalog's epistemic temperature where it had run hot — Witness stops being described as if it already runs, candidate patterns are named as such, and the verification cluster's claim is bounded to what measurement can establish — while raising precision where it matters: a formal definition of ontology, a worked behavioural-inference example, and the explicit expert-advisor split (deterministic measurement, advisory interpretation, human ratification) carried consistently through Patterns 16, 17, and 18.

---

## [v1.0.16] — 2026

### Pattern 14 (*Twin Verification*) deepened: choosing the comparison plane — command vs. fidelity — and faithfulness made representational, not only semantic

A focused content revision in Part III. Pattern 14 (*Twin Verification*) gains an explicit treatment of a problem the original framing glossed: once the modern target is more than a transliteration of the legacy, "run both against the same inputs and compare outputs" hides a real impedance mismatch. A CICS transaction is driven by a flat COMMAREA and mutated VSAM/DB2 state; a Wolverine vertical slice is driven by typed commands and expresses itself as domain events. They cannot be compared without a translation layer — an anti-corruption layer — and *which side it wraps* determines the vocabulary equivalence is judged in. The pattern now names two comparison planes and argues a complete verification story uses both.

**Manuscript:**
- **Pattern 14 (*Twin Verification*)** — Context generalised so the verified unit varies *with altitude*: early on a single translated paragraph, later the end-to-end behaviour of a whole [vertical slice](#gl-vertical-slice) as paragraphs assemble into a feature
- Forces — faithfulness reframed as not only **semantic** but **representational**: the legacy and the modern target rarely speak the same language, so the comparison cannot happen until the team decides *in which representation* equivalence is judged, a decision that shapes both what the verification proves and what the test corpus is worth once the legacy is gone
- New ***Choosing the comparison plane*** subsection:
  - the **command plane** (the primary one, implemented in Rosetta) — the ACL wraps the *Twin*, the test corpus is authored as typed commands with expected events, comparison happens in the surviving [ubiquitous language](#gl-ubiquitous-language); it outlives oracle retirement and seeds the Pattern 16 behavioural specs, and the COMMAREA-shaped translation is quarantined on the side scheduled for deletion (the difference between an anti-corruption layer and *Jobol*)
  - the **fidelity plane** (planned) — driven by *real captured COMMAREA traffic* rather than fabricated input, closing the dangerous gap where translating a command *down* into a COMMAREA manufactures assumption-laden bytes; replays production-recorded inputs through Twin and slice and compares in the legacy's observable projection, catching the undocumented quirks no authored test would encode; outbound projection deliberately lossy in the safe direction (richer modern output = intended divergence)
  - one transitional ACL serves both planes and the Pattern 27 dual-run boundary, and like every transitional structure is built to be removed; the intended-vs-real divergence call is framed as the expert-advisor work of Patterns 12–13 turned on the diff — the agent makes the judgement *affordable* across thousands of fields; the human ratifies
- New diagram `diagram-twin-planes.png`
- PDF and EPUB regenerated

**README:**
- Status badge bumped from `v1.0.15` to `v1.0.16`
- PDF and EPUB download links point to the `v1.0.16` release

**Net effect:** ~+16/−2 lines in the manuscript, concentrated entirely in Pattern 14. Pattern count remains 28; no renumbering, no structural change. The verification story stops assuming the legacy and the modern target are directly comparable and names the anti-corruption layer the comparison actually runs through — making explicit that *which vocabulary equivalence is judged in* is a design decision, that authored command-plane tests and replayed fidelity-plane tests answer two different questions, and that the corpus authored in the surviving language is what remains when the oracle retires.

---

## [v1.0.15] — 2026

### Part II ("Tactical Generation") rebuilt around what decomposition introduces; the compiler principle, the IR, and the distribution patterns substantially deepened

A substantive content revision concentrated in Part II. The part gains an explicit *two-movement* framing — *generation* (Patterns 7–10: how aggregates, events, and handlers are produced and rendered) and *what decomposition introduces* (Patterns 11–13: the costs of splitting a co-located legacy into separately-deployed contexts). Two patterns are renamed to say what they are about, and the three tactical-distribution patterns are rewritten to treat the distributed system as a thing the modernization *creates*, not merely inherits. The Preface gains a standing "living essay" status note. Pattern 6 is sharpened with the concrete mainframe signature of each Evans relationship type.

**Manuscript:**
- Preface — new ***Status of this draft*** note up front: the catalog is a *living essay of first learnings, to be refined*, every claim a hypothesis offered to be tested, the version's date marking where the thinking stands rather than where it ends
- Part II opener — rewritten around **two movements**: *generation* (the compiler principle divides deterministic from probabilistic work, the IR is the contract, tier-aware scaffolding picks the architecture, pluggable emitters render it) and *what decomposition introduces* (logical boundary, transactional guarantees, the network), naming why the three distribution patterns exist
- **Pattern 7 (*The Compiler Principle*)** — Context and Problem substantially expanded: *LLMs as compilers, not interpreters* named as the converged community position (economic, architectural, and operational lessons); determinism reframed as imposed **by construction vs. by rejection**; the finding that the **harness around a model can swing benchmark results 30–50 points** — reliability is a property of the architecture, not the model; prompts are advisory, not contracts
- **Pattern 8 (*The Intermediate Representation*)** — new third tension (**authorship**: judgement to be frozen vs. mechanical structure); a full **worked example** — a `2100-VALIDATE-CLAIM` paragraph projected to an IR-DOMAIN `HandlerIntent` (serialized YAML the architect reviews and freezes) and the IR-SCAFFOLD C# shell it deterministically projects; IR-Domain made explicitly *commitment-encoding* (`HandlerIntent`→VSA, `PortIntent`→Hexagonal, `SagaIntent`→event-driven)
- **Pattern 11** — renamed *Commands and Events as Logical Boundary, Independent of Physical Deployment* → ***Commands and Events as the Logical Boundary***; rebuilt around **modular-monolith-first** plus an **agentic evolution loop** (probabilistic proposal → human-on-the-loop approval → deterministic execution), with the logical boundary, enforced by construction, as what makes physical re-topology *safe*
- **Pattern 12 (*Transactional Boundaries*)** — agents reframed as a **panel of expert advisors, not decision-makers**, their tasks placed on the deterministic-probabilistic spectrum (advisory analysis vs. fully deterministic IR validation); *saga* and *Wolverine* glossary links added
- **Pattern 13** — renamed *Temporal Decoupling and Latency-Aware Data Access* → ***Distribution Introduces a Network***; rebuilt around **Deutsch's fallacies of distributed computing** (1994), with the *reliability* dimension (timeout-as-designed-value, retry-only-where-idempotent, circuit breakers/bulkheads, explicit handling of the indeterminate outcome) made co-equal with latency; the **chatty cursor** recast as the N+1 ancestor; a two-level agent analysis (tactical pattern-matching inspection + advisory reasoning) naming Polly and Dapr-style resiliency
- **Pattern 6 (*Context Map for Modernization*)** — each Evans relationship type given its concrete **mainframe signature** (shared copybook → shared kernel; `EXEC CICS LINK`/`START` → customer-supplier; COMMAREA/channel → published language; flat-file/MQ → ACL; shared VSAM/DB2 → the hardest boundary); three-population framing trimmed toward business contexts and their durable external-vocabulary relationships; new context-map diagram
- PDF and EPUB regenerated

**README:**
- Status badge bumped from `v1.0.14` to `v1.0.15`
- PDF and EPUB download links point to the `v1.0.15` release

**Net effect:** ~+371 lines added, ~−260 removed in the manuscript. Concentration in Part II — the compiler principle, the intermediate representation, and the three distribution patterns (11–13) — plus the Preface status note and Pattern 6's mainframe signatures. Pattern count remains 28; no renumbering, no new parts. Part II stops treating the distributed system as inherited and names it as something the modernization builds: the logical boundary that makes topology evolution safe, the transactional guarantees that must be carried deliberately across it, and the network whose two fallacies — latency and reliability — must be engineered rather than assumed away.

---

## [v1.0.14] — 2026

### Retitled *Agentic Domain-Driven Mainframe Modernization*; Pattern 6 rebuilt as a temporal, three-population context map; a *Further Reading* chapter added

A major release. The catalog is **retitled from *AI-Assisted Domain-Driven Mainframe Modernization* to *Agentic Domain-Driven Mainframe Modernization*** — a change of identity, not just of words. The cover, the citation, the repository's manuscript filename, and the release assets all carry the new name. "AI-assisted" is retained as a *descriptive* phrase where it names the activity (the two theses, the epigraph, the per-capability strategy table); what changed is the book's own name. The release also lands the largest single-pattern expansion since v1.0.11 and the catalog's first dedicated bibliography. Pattern 6 (*Context Map for Modernization*) is rebuilt around three ideas that were previously implicit: the context map is **temporal** (relationship types change as contexts transition, each stage named with the criterion for moving to the next), it is **populated by three distinct kinds of bounded context simultaneously** — modernized business contexts, agentic-platform contexts (Pattern 19's MCP servers and the LLMs themselves, treated as bounded contexts in the canonical Evans sense, citing Evans' *Context Mapping with an AI-based Component*, 2026), and external-vocabulary contexts (NAICS, BIAN, FIBO, ACORD, GS1) — and it is **readable as a migration plan**, since each Evans relationship type implies a specific operational pattern, so sequencing the migration becomes sequencing the transitional relationships. The transitional-vs-durable distinction is made first-class: every transitional relationship (ACL, bridge API, conformist accommodation) carries a named retirement criterion, turning transitional architecture from "a fog into a backlog."

**Manuscript:**
- **Retitled** *AI-Assisted Domain-Driven Mainframe Modernization* → ***Agentic Domain-Driven Mainframe Modernization*** (title page, running identity, citation block; manuscript file renamed accordingly)
- Preface — new opening paragraph framing the book as the long form of the argument the author makes at the start of every engagement, against the promise that the hard part can be skipped ("feed in the COBOL, receive clean Java")
- Preface — new paragraph on **DDD as the most underestimated discipline in software**, with Jacob Burckhardt's "the essence of tyranny is the denial of complexity" recast for modernization: the complexity of a forty-year-old system is not an obstacle to the work, it *is* the thing being modernized; the catalog as an argument against silver bullets
- Pattern 6 (*Context Map for Modernization*) — substantially expanded: the context map made **temporal** (relationship types transition through stages with explicit move-on criteria), **three-population** (business / agentic-platform / external-vocabulary contexts on one map; LLM-as-bounded-context citing Evans, 2026), and **derivable as a migration plan** (each Evans relationship type → its operational pattern in Patterns 11/24/27/28); transitional-vs-durable distinction with per-relationship retirement criteria made first-class; default failure modes named (inherited conformist, accidental shared kernel, separate-ways-treated-as-failure, immortal ACLs, fully-connected mesh); subdomain identity established as the constraint on which relationship types are coherent
- Pattern 15 (*Hypothesis-Driven Verification*) — new subsection ***Verifying boundaries, not only behaviour***: the linguistic bounded-context test made an agentic verification assessment that checks a candidate boundary's vocabulary against the ontology, surfacing where terms stay coherent, shift at the edge (confirming the boundary), or shift within it (contradicting it) — consumed by Pattern 6 as a boundary signal
- New chapter ***Further reading*** — the catalog's first dedicated bibliography, grouping cited works by the three traditions (Domain-Driven Design; AI engineering for agentic systems; Legacy and mainframe modernization) plus *Adjacent and supporting* and *Community resources*, with a candid note that bibliographic detail is orienting rather than citation-precise
- Systematic **inline glossary hyperlinks** added throughout the manuscript (`[bounded contexts]`, `[ubiquitous language]`, `[anti-corruption layer]`, `[strangler fig]`, `[tactical design]`, and many more linking to their glossary anchors)
- PDF and EPUB regenerated under the new title

**README:**
- Title and citation retitled to *Agentic Domain-Driven Mainframe Modernization*
- Status badge bumped from `v1.0.13` to `v1.0.14`
- Download links and asset filenames updated to `v1.0.14` and `Agentic.Domain-Driven.Mainframe.Modernization.{pdf,epub}`; Markdown-source link updated to the renamed manuscript

**LICENSE:**
- Citation block retitled to *Agentic Domain-Driven Mainframe Modernization*

**Net effect (excluding typographic normalisation):** ~+222 lines added, ~−137 removed; net ~+85 lines of real content. Concentration in Pattern 6 (temporal, three-population, migration-plan context map), the new *Further Reading* chapter, and two new Preface paragraphs; the remainder is inline glossary linking. Pattern count remains 28; no renumbering, no new parts. The retitling means readers citing an earlier-numbered edition are citing a differently-named book — and the release also lands a new top-level chapter and the largest pattern expansion since the GraphRAG rewrite.

---

## [v1.0.13] — 2026

### Pattern-language craft named in the Preface; cross-pattern semantics sharpened across Patterns 4, 5, 6, 19, and 28

A substantive content revision that strengthens the Preface's framing and tightens the relationships *between* patterns rather than rewriting any one of them. The Preface gains two notes: one on what pattern languages are *for* — naming recurring forms so the long, multi-team work of modernization becomes a tractable shared conversation, the elephant addressable one named bite at a time (Alexander; Gamma, Helm, Johnson, Vlissides, 1994) — and a second epistemic note on the catalog itself doing vocabulary work, choosing words for a territory (mainframe modernization × AI engineering × contemporary DDD) where the names are still being settled. Four cross-pattern semantic links are made first-class: **published languages already exist in the legacy, undeclared** (Pattern 4) and the **ACL is the runtime artifact of a transitional published language** with its own lifecycle (Pattern 28) — recovery, defensive, bridging, authority shift, decommission; **the side-effect surface of a slice is its candidate seam set, viewed from outside** (Pattern 5) and **slices that share side-effects belong to the same bounded context** — side-effect clustering as boundary evidence complementary to vocabulary clustering (Pattern 6); **Conway's Law as the origin condition of bounded contexts in a legacy mainframe** — context recovery reframed as organisational archaeology (Pattern 19). A published-language *strategy table* is added to Pattern 4: generic subdomains *adopt* an industry standard (NAICS, FIBO, ACORD, GS1, ISO), core subdomains *invent*, supporting subdomains *adapt*.

**Manuscript:**
- Preface — new paragraph on pattern languages as shared, unambiguous vocabulary for multi-team modernization (Alexander; GoF, 1994); the "elephant becomes addressable, one named bite at a time" framing
- Preface — new epistemic note that the catalog is shaping the vocabulary, not just the patterns; explicit acknowledgement that some terms here will persist and others will be replaced as the field converges
- Pattern 4 (*Domain Ontology as Independent Substrate*) — added: **published languages already exist in the legacy, undeclared** (DCLGEN copybooks, COMMAREA layouts, batch-step file formats, queue message schemas fit Evans' definition exactly); recovery is the first move, formalisation the second
- Pattern 4 — added: **published-language strategy by subdomain type** — generic→adopt, core→invent, supporting→adapt; strategic-design choice (Pattern 1) and downstream determinant of Pattern 9 scaffold
- Pattern 5 (*Slice and Seam Discovery*) — sharpened: **the side-effect surface of a slice is its candidate seam set, viewed from outside** (same set of points described from slice interior and exterior respectively)
- Pattern 6 (*Context Map for Modernization*) — added: bounded-context boundaries recovered from *multiple* signals — side-effect clustering as boundary evidence complementary to vocabulary clustering; operational coupling matters as much as linguistic alignment
- Pattern 19 (*Team Topology and Bounded Context Alignment*) — added: **Conway's Law as the origin condition** of bounded contexts in the legacy; the implicit published languages of Pattern 4 are the protocols the original teams negotiated; context recovery reframed as organisational archaeology
- Pattern 28 (*Dual-Run Coexistence*) — added: **the ACL is the runtime artifact of a transitional published language**, with a lifecycle — discovery, defensive, bridging, authority shift, decommission; a bridge API that does not eventually retire signals an incomplete modernization or a misjudged boundary
- PDF and EPUB regenerated

**README:**
- Status badge bumped from `v1.0.12` to `v1.0.13`
- PDF and EPUB download links point to the `v1.0.13` release

**Net effect (excluding typographic normalisation):** ~+15 lines added, ~−1 removed. Seven new paragraphs, no structural changes, pattern count remains 28; no renumbering, no new parts. The catalog stops treating the *relationships* between patterns as implicit and names them: side-effects show up as both seams (5) and boundaries (6); published languages show up as both pre-existing legacy artifacts (4) and the protocols ACLs operationalise during transition (28); Conway's Law shows up both backward (as the system that laid down the implicit contexts) and forward (as the system that will lay down the next ones).

---

## [v1.0.12] — 2026

### Pattern 5 widened to *Slice and Seam Discovery*; Pattern 4 reframed around language and published-language taxonomies

A substantive content revision focused on the strategic-recovery patterns. Pattern 5 is renamed and rebuilt from *Vertical Slice Discovery* to ***Slice and Seam Discovery from Structural and Behavioural Signals*** — the pattern now produces *paired* outputs from one shared multi-signal pipeline: **slices** (semantic units of value, what to migrate) and **seams** (technical intervention points, where to cut in). Michael Feathers' seam concept (*Working Effectively with Legacy Code*, 2004) is brought in as named lineage; Ian Ferri & Rob Coggrave's *Uncovering the Seams in Mainframes for Incremental Modernisation* (martinfowler.com, 2024) supplies the eight-type mainframe seam typology — two external (batch input, API access) and six internal (data interactions, DB readers, DB writers, batch pipeline step handoff, data characteristic, downstream processing handoff). Pattern 4 (*Domain Ontology as Independent Substrate*) is rewritten around DDD as a discipline about language: Evans' distinction between **ubiquitous language** (within a bounded context) and **published language** (between contexts, *Domain-Driven Design* p. 330) is made first-class, and industry taxonomies — **BIAN, FIBO, ACORD, GS1, NAICS** — are introduced as canonical published-language examples and treated as a strategic-design choice.

**Manuscript:**
- Pattern 5 renamed *Vertical Slice Discovery* → ***Slice and Seam Discovery from Structural and Behavioural Signals***; produces paired outputs (slice maps, seam-typology tables, dependency overlays) from one pipeline; signal sources grow from five to six (semantic similarity from Pattern 3's index added as its own signal); four *good-seam criteria* (observable, divertable, externally usable, funnel-like) made explicit; integration patterns each seam uses — Event Interception, Legacy Mimic, Extract Product Lines, Dark Launching, Canary Release — credited to Newman *et al.*'s *Patterns of Legacy Displacement* (martinfowler.com); Eric Holden's *Eating the Elephant* credited for programme-mobilisation framing
- Pattern 4 substantially rewritten — Context reframed around DDD as a discipline about language; **published language** introduced as first-class, distinct from ubiquitous language, with industry taxonomies as canonical examples; Forces enumerates four recovery input classes (domain experts, business artifacts, industry taxonomies, operational knowledge); substrate reframed as cognitive infrastructure supporting *knowledge crunching*, *disambiguation*, *boundary evidence*, and *debt management* (technical and cognitive debt distinguished); independence reframed as separation of concern, not infrastructure (implemented within the same GraphRAG substrate as Pattern 3); closing scope note acknowledging seam discovery will be named as its own pattern in a forthcoming revision
- Pattern 3 (*The Graph as Projection*): vocabulary recovery deferred from Pattern 3 to Pattern 4; *Related patterns* updated to acknowledge semantic similarity now feeds seam discovery in addition to slice discovery
- Preface: new paragraph naming what this catalog is and isn't — explicit acknowledgement that the work links three fast-moving traditions (AI engineering for agentic coding, contemporary DDD, legacy modernization), with Feathers, Fowler's strangler fig, Newman, Tune, Ferri & Coggrave, and Holden named as the literatures being drawn together
- Lineage roll-call in *How to read this catalog* extended: Feathers, Ferri, Coggrave, Holden added
- Glossary: new entry ***Seam*** (Feathers; Ferri & Coggrave's eight-type mainframe typology and four good-seam criteria); cross-references in *Vertical slice* and *Event Storming* entries updated to *Slice and Seam Discovery*
- Cross-references to the former *Vertical Slice Discovery* updated catalog-wide (Patterns 1, 3, 16, 21; pattern-engagement spectrum table; antipattern reference table; Reference Implementations section)
- PDF and EPUB regenerated

**README:**
- Status badge bumped from `v1.0.11` to `v1.0.12`
- PDF and EPUB download links point to the `v1.0.12` release

**Net effect (excluding typographic normalisation):** ~+180 lines added, ~−95 removed; net ~+85 lines of real content. Concentration in Pattern 5 (paired slice/seam discovery) and Pattern 4 (published language and industry taxonomies). Pattern count remains 28; no renumbering, no new parts. Pattern 5 stops being a slice-only discovery and becomes the joint discovery of *what to migrate* and *where to intervene*; Pattern 4 stops treating ontology as a data-model concern and names language — ubiquitous within a context, published between them — as the substrate the modernization is building.

---

## [v1.0.11] — 2026

### Pattern 3 rewritten around GraphRAG; operational evidence as first-class L1 input

A substantive content revision focused on Pattern 3 (*The Graph as Projection*). The pattern is reframed around **GraphRAG** as its named architectural ancestor — Microsoft's research initiative and Anthony Alcaraz's *agentic GraphRAG* framing are credited explicitly as the lineage this catalog instantiates for legacy mainframe modernization. The L1/L2 graph-layer model is sharpened, the AST → property-graph derivation is made explicit (ANTLR named as the typical tool), and operational artifacts (SMF records, CICS CSD/RDO transaction maps, JCL job streams) are promoted to first-class L1 inputs alongside source. The copy-paste-programming argument for semantic similarity is made concrete with a `B100-VALIDATE-CUSTOMER` / `C100-VERIFY-CLIENT` example. A Cypher query example shows how the two substrates compose at retrieval time. Chris Richardson's fabrication-failure observation is named directly. Cross-references are updated to point at Pattern 6, Pattern 19, Pattern 21, and Pattern 22.

**Manuscript:**
- Pattern 3 (*The Graph as Projection*) substantially rewritten — opens with a million-line-of-COBOL framing, names the substrate question, threads GraphRAG as the pattern lineage, makes the L1/L2 distinction structural rather than incidental, and treats SMF / CSD / RDO / JCL as L1 inputs
- Added concrete Cypher example showing a hybrid graph-traversal-into-index-retrieval composed as one query
- Reframed *Consequences* around the substrate as a navigable lens for human comprehension, with agents translating intention into queries the substrates serve
- Source provenance reframed as a structural property of both substrates, not a discipline bolted on
- Glossary additions: **Embedding**, **Semantic index**, **Vector database** — the implementation vocabulary Pattern 3 now uses directly
- PDF and EPUB regenerated

**README:**
- Status badge bumped from `v1.0.10` to `v1.0.11`
- PDF and EPUB download links point to the `v1.0.11` release

**Net effect:** ~45 lines added, ~28 lines removed in the manuscript. Pattern 3 stops being a generic dual-substrate argument and becomes a named instance of a recognised pattern (GraphRAG) calibrated to mainframe modernization, with the operational artifacts that mainframe estates actually produce as evidence brought into the substrate explicitly.

---

## [v1.0.10] — 2026

### First stable release; Rosetta Stone framing recast as an opening epigraph

The catalog leaves draft. The Rosetta Stone analogy — previously a prose paragraph inside the Preface explaining why the project is named *Project Rosetta* — is lifted to the front matter as a short verse epigraph that opens the book, set immediately before the dedication. The explanatory paragraph is removed from the Preface so the framing is stated once, as an inscription, rather than argued in exposition.

**Manuscript:**
- New opening epigraph: the Rosetta Stone framing rendered as a six-line verse, placed before the dedication
- The "*The name Project Rosetta is deliberate…*" paragraph removed from the Preface (its meaning now carried by the epigraph)
- PDF and EPUB regenerated
- Post-release fix: the Journey and Antipatterns chapter-opener plates were transposed in the initial v1.0.10 build; corrected source images regenerated and the v1.0.10 release assets replaced in place

**README:**
- Status badge changed from `draft v1.0.9` (orange) to `v1.0.10` (green) — out of draft, first stable release
- PDF and EPUB download links point to the `v1.0.10` release

---

## [v1.0.9] — 2026

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

## [v1.0.8] — 2026

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

## [v1.0.7] — 2026

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

## [v1.0.6] — 2026

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

## [v1.0.5] — 2026

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

## [v1.0.4] — 2026

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

## [v1.0.3] — 2026

### Housekeeping — README and repository hygiene

Updated README to reflect the v1.0.2 release and improved repository setup.

**Changes:**
- Updated status badge from `draft v1.0.0` to `draft v1.0.2`
- Updated PDF and EPUB download links to point to v1.0.2 release assets on GitHub
- Added Uberto Barbini to the contributors list in the README
- Added `.gitignore` to exclude `.claude/` directory from version control

---

## [v1.0.2] — 2026

### Uberto Barbini's contributions integrated

Integrated Uberto Barbini's work on agent execution discipline and failure modes into the catalog. Three areas of contribution: the *one prompt, one commit* principle as a unit-of-change discipline for agent-produced work, the taxonomy of agent execution failure modes (*loop of death*, *misunderstanding the requirement*, *desperate changes*) with detection and corrective mechanisms at platform scale, and the idea of deriving heuristic catalog entries from operational history (git history and PR comments as input to agent rules).

**Changes:**
- Pattern 22 (Heuristics as Explicit Artifacts): added paragraph on deriving catalog entries from operational history, referencing Barbini's experiments with generating rule files from git history and PR comments
- Pattern 23 (The Harness as Self-Observing State Machine): added paragraph on *one prompt, one commit* principle as unit-of-change discipline; added paragraph on agent execution failure modes with platform-scale detection mechanisms (cycle detection, scaffold-boundary violation, invariant violation)
- Glossary: added *Agent execution failure modes* entry defining loop of death, misunderstanding the requirement, and desperate changes, with cross-references to Patterns 22 and 23
- Added Uberto Barbini to the contributors list in the introduction and lineage section
- Updated epub and pdf artifacts

---

## [v1.0.1] — 2026

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

## [v1.0.0] — 2026

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
