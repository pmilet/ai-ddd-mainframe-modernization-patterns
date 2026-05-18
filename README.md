# AI-Assisted Domain-Driven Mainframe Modernization

## A Pattern Catalog from Project Rosetta

[![Status](https://img.shields.io/badge/status-draft%20v0.8-orange)](https://github.com/pmilet/ai-ddd-mainframe-modernization-patterns/releases)
[![License](https://img.shields.io/badge/license-CC%20BY%204.0-blue)](LICENSE)

Kent Beck's **3X** framework names three modes of software work: **Explore** — search for something that works, where most bets fail and learning is the only reliable return; **Expand** — scale what worked once demand is real; **Extract** — flatten costs once the shape is stable. This catalog is Explore, deliberately and entirely: twenty-eight patterns where Domain-Driven Design meets AI-assisted blackfield mainframe modernization, none yet put under load by a real customer engagement at production scale. That is Expand — the next phase, not this one.

This is the long version of what I've been writing about on LinkedIn under the [LegacyLabs](https://www.linkedin.com/newsletters/legacy-labs-7317839126702055426/) name. The shorter posts and newsletter there were the introduction.

---

## Download

| Format | Description |
|--------|-------------|
| 📄 [**PDF**](https://github.com/pmilet/ai-ddd-mainframe-modernization-patterns/releases/download/v0.8/AI-Assisted.Domain-Driven.Mainframe.Modernization.pdf) | Full catalog, print-friendly |
| 📱 [**EPUB**](https://github.com/pmilet/ai-ddd-mainframe-modernization-patterns/releases/download/v0.8/AI-Assisted.Domain-Driven.Mainframe.Modernization.epub) | E-reader format (Kindle, Kobo, Apple Books) |
| 📝 [**Markdown source**](AI-Assisted%20Domain-Driven%20Mainframe%20Modernization.md) | Read directly on GitHub |

---

## What this catalog is

A pattern catalog for AI-assisted modernization of COBOL/CICS mainframe systems, written through a Domain-Driven Design lens. The thesis: **AI-assisted mainframe modernization is, at its core, a Domain-Driven Design activity at scale**. AI agents accelerate the mechanical parts; humans direct the strategic ones; the boundary between agentic and human work is itself an architectural commitment that needs explicit design.

The catalog is a mix of three kinds of patterns:

- **Original patterns** — practices that emerged from building Project Rosetta and that the field has not yet articulated as patterns in their own right
- **Adapted patterns** — established practices applied to mainframe modernization with explicit recalibration
- **DDD re-articulations** — canonical DDD patterns recast through the lens of legacy mainframe modernization

It stands on shoulders — Eric Evans, Vaughn Vernon, Martin Fowler, Sam Newman, Alberto Brandolini, Vlad Khononov, Cyrille Martraire, Birgitta Böckeler, Charity Majors, Nick Tune, Uberto Barbini, Kent Beck, Matthew Skelton, Manuel Pais, Pramod Sadalage — and names them as it builds.

---

## Maturity

This catalog is an early articulation, not a manual for proven practice. Some patterns are exercised inside the Rosetta prototype with concrete implementation behind them; others are reasoned forward from validated principles — the architecture is grounded, but the specific pattern has not yet been run against real code. Each pattern's body says which, in prose, rather than through a status label.

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

Pierre Milet Llobet is a software architect at Microsoft, with fifteen years of mainframe modernization experience. He came to mainframes as an outsider and learned the COBOL/CICS world the slow way — through migrations done before AI assistance was practical, when modernization was a matter of careful manual work. **Project Rosetta** is the experiment in what becomes possible when AI assistance changes that economics. The patterns here are reports from inside that experiment.

He writes about modernization, AI-assisted software engineering, and Domain-Driven Design under the [LegacyLabs](https://www.linkedin.com/newsletters/legacy-labs-7317839126702055426/) name on LinkedIn.

---

## License

This work is licensed under [Creative Commons Attribution 4.0 International (CC BY 4.0)](LICENSE).

You are free to share and adapt the material for any purpose, even commercially, under the condition that you give appropriate credit to the author, provide a link to the license, and indicate if changes were made.

---

## Citation

If you reference this catalog in academic, professional, or commercial work, please cite as:

> Milet Llobet, P. (2026). *AI-Assisted Domain-Driven Mainframe Modernization: A Pattern Catalog from Project Rosetta*. LegacyLabs. https://github.com/pmilet/ai-ddd-mainframe-modernization-patterns

---

*Twenty-eight patterns. More is not better. Less is better.*
