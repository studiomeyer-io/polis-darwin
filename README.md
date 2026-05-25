# Polis

> 5 KI-Agenten bauen eine kleine Stadt.

Polis ist eine offene Multi-Agent-Society-Simulation. Fuenf Claude-LLM-Rollen (Buergermeister, Haendler, Bauer, Forscher, Kuenstler) leben in einer kleinen Stadt, treffen Entscheidungen, verhandeln, scheitern, lernen.

Inspiriert von [Smallville](https://arxiv.org/abs/2304.03442), [Voyager](https://arxiv.org/abs/2305.16291), [GovSim](https://arxiv.org/abs/2404.16698), [AgentVerse](https://arxiv.org/abs/2308.10848) und [Project Sid](https://altera.al/research). Laeuft lokal, nutzt Claude-Subscription statt API-Credits, Code wird ab V2.0 (geplant 2026 Q3) hier offen sein.

**Live-Showcase:** [meetmyagent.io](https://meetmyagent.io)

---

## Stack

| Layer | Paket |
|---|---|
| Multi-Agent Runtime | [darwin-agents](https://github.com/studiomeyer-io/darwin-agents) 0.5.0-alpha.2 |
| Graph Orchestration | [@langchain/langgraph](https://github.com/langchain-ai/langgraphjs) 1.3 |
| Darwin LangGraph Adapter | [darwin-langgraph](https://github.com/studiomeyer-io/darwin-langgraph) 0.3.0-alpha.1 |
| Tracing | [Langfuse + langfuse-langchain](https://langfuse.com) |
| LLM | Claude CLI Subscription (Sonnet 4.6) |
| Validation | Zod |

## Welt-Mechaniken

- **Shared Commons** — Felder regenerieren langsam, Ueberernte kostet Stimmung (GovSim)
- **Veto-Demokratie** — jede Bau-Entscheidung laeuft als Pledge, andere Rollen koennen unterstuetzen oder vetoen (AgentVerse)
- **Skill-Library** — Forscher archiviert verifizierte Learnings, naechster Run startet smarter (Voyager)
- **Whisper-Channel** — Rollen koennen leise miteinander reden ohne dass alle es lesen (Smallville)
- **Inspire-Broadcast** — Kuenstler beeinflusst Mood-Pool global
- **Reisender** — kommt Tick 10-15 mit unerwarteter Nachricht von ausserhalb
- **Krise** — bei 50% Run-Fortschritt schlaegt etwas Schweres ein

## Status

| Version | Status | Was |
|---|---|---|
| V1.0 | DONE | Prototyp lokal, 5 Ticks ohne Collapse, Chronik scored erste Story |
| V1.1 | DONE | R1+R2 agent-code-review GO, 15 Fixes, evolution-snapshot, kanonische Doku |
| V1.2 | DONE (2026-05-25) | Public-Spiegel + Coming-Soon-Site auf meetmyagent.io live |
| V2.0 | next | Live-Showcase: Phaser-Town, /agent-Drilldown, SSE-Stream — Code-Drop hier |
| V2.1 | planned | Run-Queue (max 3 parallel), Run-Historie, Permalink fuer einzelne Ticks |
| V3 | planned | NPCs (Architekt, Grafiker, Reisende), AI-Town-Style Karte |
| V4 | planned | Three.js 3D-Stadt + Temporal fuer Multi-Tick Build-Workflows |

## Roadmap

Polis lebt aktuell als Prototyp im [StudioMeyer Nex-HQ Monorepo](https://github.com/studiomeyer-io). Code-Drop in dieses Repo passiert zur V2.0. Wer den V1-Code vorab sehen will: Mail an `matthias@studiomeyer.io`.

## Forschungs-Notiz

Kanonische Forschungs- und Architektur-Notiz: [meetmyagent.io](https://meetmyagent.io). Eine sauber refaktorierte Variante des V1-Research-Reports zu Multi-Agent-Society-Patterns (Smallville/Voyager/GovSim/AgentVerse/Project Sid) wird mit V2.0 hier veroeffentlicht.

## Lizenz

MIT (sobald Code-Drop V2.0). Bis dahin: Konzept + Roadmap frei verwendbar mit Quellennennung.

---

Built by [Matthias Meyer](https://studiomeyer.io) · [Studio](https://github.com/studiomeyer-io) · 2026
