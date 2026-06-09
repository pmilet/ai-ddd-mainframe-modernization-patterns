# Agentic Domain-Driven Mainframe Modernization

## A Pattern Catalog from Project Rosetta

[![Status](https://img.shields.io/badge/status-v1.2.1-brightgreen)](https://github.com/pmilet/ai-ddd-mainframe-modernization-patterns/releases)
[![License](https://img.shields.io/badge/license-CC%20BY%204.0-blue)](LICENSE)

Mainframe modernization is usually treated as a code problem. It's a domain problem — the richest business logic in the enterprise, buried in decades of COBOL, waiting to be recovered. Domain-Driven Design was built for exactly that. The two have rarely met.

The hard part of modernizing a mainframe was never translating the COBOL. It's recovering what the system *means* — the business concepts the code accumulated and never wrote down. That is a domain problem before it is a code problem, and it is precisely what DDD was made for.

This catalog is for doing exactly that: twenty-eight patterns and an antipatterns chapter for AI-assisted modernization of COBOL/CICS mainframe systems, read through a Domain-Driven Design lens — with AI agents working inside a harness rather than driving the work. The patterns name the recurring problems and the solutions worth trying, so hard-won lessons become transmissible — codified in a form that invites discussion and debate rather than prescribing a recipe.

They come from Project Rosetta, a working experiment in what AI assistance changes about modernization economics, and are written for DDD practitioners, mainframe modernization practitioners, and AI engineers working at the frontier of agentic coding.

A shorter **companion essay**, *The Rosetta Conjecture: Domain-Driven Agentic Modernization*, runs alongside the catalog and is now available in **English, Spanish, and French**. It is the principles-first argument behind the patterns: the domain at the centre, the architect's elevator with agents on every floor, and Kent Beck's 3X model placing this work declaredly in Explore. Where the catalog names twenty-eight situated patterns, the essay reasons in plain prose about why a method ought to work — *modernizing is not translating code; it is recovering the domain.* Read the essay for the argument; read the catalog for the patterns.

This is the long version of what I've been writing about on LinkedIn under the [LegacyLabs](https://www.linkedin.com/newsletters/legacy-labs-7317839126702055426/) name. The shorter posts and newsletter there were the introduction.

---

## Download

**Pattern catalog** — twenty-eight patterns, an antipatterns chapter, reference implementations.

| Format | Description |
|--------|-------------|
| 📄 [**PDF**](https://github.com/pmilet/ai-ddd-mainframe-modernization-patterns/releases/download/v1.2.1/Agentic.Domain-Driven.Mainframe.Modernization.pdf) | Full catalog, print-friendly |
| 📱 [**EPUB**](https://github.com/pmilet/ai-ddd-mainframe-modernization-patterns/releases/download/v1.2.1/Agentic.Domain-Driven.Mainframe.Modernization.epub) | E-reader format (Kindle, Kobo, Apple Books) |
| 📝 [**Markdown source**](Agentic%20Domain-Driven%20Mainframe%20Modernization.md) | Read directly on GitHub |

**Companion essay** — *The Rosetta Conjecture: Domain-Driven Agentic Modernization.* The principles-first argument that sits behind the patterns, available in three languages.

| Language | PDF | EPUB | Markdown |
|----------|-----|------|----------|
| **English** — *The Rosetta Conjecture* | 📄 [PDF](https://github.com/pmilet/ai-ddd-mainframe-modernization-patterns/releases/download/v1.2.1/The.Rosetta.Conjecture.pdf) | 📱 [EPUB](https://github.com/pmilet/ai-ddd-mainframe-modernization-patterns/releases/download/v1.2.1/The.Rosetta.Conjecture.epub) | 📝 [Source](The%20Rosetta%20Conjecture.md) |
| **Español** — *La Conjetura de Rosetta* | 📄 [PDF](https://github.com/pmilet/ai-ddd-mainframe-modernization-patterns/releases/download/v1.2.1/La.Conjetura.de.Rosetta.pdf) | 📱 [EPUB](https://github.com/pmilet/ai-ddd-mainframe-modernization-patterns/releases/download/v1.2.1/La.Conjetura.de.Rosetta.epub) | 📝 [Fuente](La%20Conjetura%20de%20Rosetta.md) |
| **Français** — *La Conjecture de Rosetta* | 📄 [PDF](https://github.com/pmilet/ai-ddd-mainframe-modernization-patterns/releases/download/v1.2.1/La.Conjecture.de.Rosetta.pdf) | 📱 [EPUB](https://github.com/pmilet/ai-ddd-mainframe-modernization-patterns/releases/download/v1.2.1/La.Conjecture.de.Rosetta.epub) | 📝 [Source](La%20Conjecture%20de%20Rosetta.md) |

---

## What this catalog is

The territory is **blackfield**: not just existing systems, but existing systems where understanding itself has been lost — the original engineers have moved on, documentation is gone, and domain knowledge has decayed into operational dialect. That is the harder case beyond brownfield, and it is why recovery comes before generation: you cannot modernize what no one can still explain.

The catalog has two theses. **First: AI-assisted mainframe modernization is, at its core, a Domain-Driven Design activity at scale.** AI agents accelerate the mechanical parts; humans direct the strategic ones; the boundary between agentic and human work is itself an architectural commitment that needs explicit design. **Second: modernization at scale is architectural reasoning under load, and AI agents reason better over architectural projections than over source code** — a property graph, a canonical ontology, an intermediate representation, a tier-aware scaffold. A third claim runs underneath both: those deterministic substrates are themselves the conceptual model agents work within, not merely inputs they consume — and so the structural harness (the typed scaffold, IR, ontology, tests) is the larger investment, not the prompts.

**Modernization is not a synonym for rewrite.** The catalog supports a strategic spectrum — rewrite, replatform with modern facade, reimagine from specifications, replace with SaaS, retire — and Pattern 1 (*Business-Aligned Capability Strategy*) is where the per-capability decision lives. The estate's technology profile after modernization is heterogeneous by design, calibrated to per-capability economics.

Every pattern follows the same shape — **Context, Problem, Forces, Pattern, Consequences, Related patterns** — and each names its own lineage as it goes: some practices emerged from building Project Rosetta; some adapt established practice to mainframe modernization with explicit recalibration; some recast canonical DDD patterns through a legacy lens. The catalog stands on shoulders — Eric Evans, Vaughn Vernon, Martin Fowler, Sam Newman, Michael Feathers, Alberto Brandolini, Vlad Khononov, Cyrille Martraire, Birgitta Böckeler, Matteo Vaccari, Charity Majors, Nick Tune, Uberto Barbini, Kent Beck, Matthew Skelton, Manuel Pais, Pramod Sadalage, Ian Ferri, Rob Coggrave, Eric Holden — and names them as it builds.

---

## Maturity

Kent Beck's **3X** framework names three modes of software work: **Explore** — search for something that works, where most bets fail and learning is the only reliable return; **Expand** — scale what worked once demand is real; **Extract** — flatten costs once the shape is stable. This catalog is Explore, deliberately and entirely.

It is a working hypothesis, not a manual for proven practice. Some patterns are exercised inside the Rosetta prototype with concrete implementation behind them — patterns in the full sense, recurring in the building. Others are reasoned forward from validated principles — the architecture is grounded, but the specific pattern has not yet been run against real production code. Each pattern's body says where it sits on that line, in prose, rather than through a status label; **a candidate pattern is not a weaker claim, it is an earlier one.** No pattern has yet been put under load by a real customer engagement at production scale — in 3X terms that is Expand, the next phase, not this one. Each pattern invites disagreement.

---

## Structure

The catalog is organised in five Parts:

- **Part I — Strategic Recovery** (Patterns 1–6): recovering the domain, identifying bounded contexts, establishing ubiquitous language, mapping context relationships
- **Part II — Tactical Generation** (Patterns 7–13): how each bounded context materialises in modern code
- **Part III — Verification** (Patterns 14–18): how the modernization knows the generated code is right — twin verification, hypothesis-driven verification, behavioural-spec inference, data-drift analysis, and the completion criteria that declare when a bounded context is done
- **Part IV — Governance and Operating Discipline** (Patterns 19–24): how the modernization stays coherent across the agentic system and the teams that operate around it
- **Part V — Safe Transition and Coexistence** (Patterns 25–28): the disciplined movement of bounded contexts from legacy authority to modernized authority, and the dual-run period during which both sides operate

Plus ten antipatterns naming the failure modes the patterns are built against.

---

## Who this is for

**DDD practitioners** will recognise vocabulary they already use — bounded contexts, ubiquitous language, subdomain types, aggregates, domain events, anti-corruption layers — and find them deployed in a domain DDD has rarely entered: mainframe modernization at decade scale.

**Mainframe modernization practitioners** less familiar with DDD will encounter the vocabulary deliberately. Where a DDD concept appears for the first time, a brief inline gloss is provided; the glossary at the end gives more complete definitions and pointers to canonical sources.

**AI engineers working at the frontier of agentic coding** will find the architectural moves familiar in shape — bounded MCP servers, hooks as constitutional enforcement, harness-over-multiplication, reasoning telemetry with faithfulness caveats — applied to a domain that AI-engineering writing rarely engages.

The catalog rewards readers from any of these three communities — though differently.

---

## Feedback welcome

This is a draft published in-progress to gather feedback while review continues. There are three ways to contribute:

- **[GitHub Issues](https://github.com/pmilet/ai-ddd-mainframe-modernization-patterns/issues)** — for specific corrections, suggestions, or questions about individual patterns
- **[LinkedIn](https://www.linkedin.com/in/pierre-milet-llobet-28827123)** — for broader discussion under the LegacyLabs name
- **[LegacyLabs newsletter](https://www.linkedin.com/newsletters/legacy-labs-7317839126702055426/)** — where the series that preceded this catalog was developed

If you find patterns I haven't articulated, antipatterns I haven't named, or contradictions I haven't resolved — please open an issue. The catalog is calibrated to what Project Rosetta has surfaced; other practitioners will find other patterns.

---

## About the author

Pierre Milet Llobet is a software architect at Microsoft, with 30+ years of software engineering experience and fifteen years of mainframe modernization. He came to mainframes as an outsider and learned the COBOL/CICS world the slow way — through migrations done before AI assistance was practical, when modernization was a matter of careful manual work. **Project Rosetta** is the experiment in what becomes possible when AI assistance changes that economics. The patterns here are reports from inside that experiment.

He writes about modernization, AI-assisted software engineering, and Domain-Driven Design under the [LegacyLabs](https://www.linkedin.com/newsletters/legacy-labs-7317839126702055426/) name on LinkedIn.

---

## License

This work is licensed under [Creative Commons Attribution 4.0 International (CC BY 4.0)](LICENSE).

You are free to share and adapt the material for any purpose, even commercially, under the condition that you give appropriate credit to the author, provide a link to the license, and indicate if changes were made.

---

## Citation

If you reference this catalog in academic, professional, or commercial work, please cite as:

> Milet Llobet, P. (2026). *Agentic Domain-Driven Mainframe Modernization: A Pattern Catalog from Project Rosetta*. LegacyLabs. https://github.com/pmilet/ai-ddd-mainframe-modernization-patterns

---

*Twenty-eight patterns. More is not better. Less is better.*
