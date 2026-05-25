# Polis

> 5 LLM agents build a small town.

Polis is an open multi-agent society simulation. Five Claude LLM roles (Mayor, Trader, Farmer, Researcher, Artist) live in a small town, make decisions, negotiate, fail, learn.

Inspired by [Smallville](https://arxiv.org/abs/2304.03442), [Voyager](https://arxiv.org/abs/2305.16291), [GovSim](https://arxiv.org/abs/2404.16698), [AgentVerse](https://arxiv.org/abs/2308.10848) and [Project Sid](https://altera.al/research). Runs locally, uses the Claude subscription instead of API credits, code will be open here from V2.0 (planned 2026 Q3).

**Live showcase:** [meetmyagent.io](https://meetmyagent.io)

---

## Stack

| Layer | Package |
|---|---|
| Multi-agent runtime | [darwin-agents](https://github.com/studiomeyer-io/darwin-agents) 0.5.0-alpha.2 |
| Graph orchestration | [@langchain/langgraph](https://github.com/langchain-ai/langgraphjs) 1.3 |
| Darwin/LangGraph adapter | [darwin-langgraph](https://github.com/studiomeyer-io/darwin-langgraph) 0.3.0-alpha.1 |
| Tracing | [Langfuse + langfuse-langchain](https://langfuse.com) |
| LLM | Claude CLI Subscription (Sonnet 4.6) |
| Validation | Zod |

## World mechanics

- **Shared commons.** Fields regenerate slowly, over-harvesting costs mood (GovSim).
- **Veto democracy.** Every build decision runs as a pledge, other roles can support or veto (AgentVerse).
- **Skill library.** The Researcher archives verified learnings, the next run starts smarter (Voyager).
- **Whisper channel.** Roles can speak quietly to each other without everyone reading along (Smallville).
- **Inspire broadcast.** The Artist nudges the global mood pool.
- **Traveler.** Arrives at tick 10-15 with unexpected news from outside.
- **Crisis.** At 50% run progress something heavy hits.

## Status

| Version | Status | What |
|---|---|---|
| V1.0 | done | Local prototype, 5 ticks without collapse, Chronicle scored first story |
| V1.1 | done | R1+R2 agent code review GO, 15 fixes, evolution snapshot, canonical docs |
| V1.2 | done (2026-05-25) | Public mirror + coming-soon site on meetmyagent.io |
| V2.0 | next | Live showcase: Phaser town, /agent drill-down, SSE stream &mdash; code drop here |
| V2.1 | planned | Run queue (max 3 parallel), run history, permalink for individual ticks |
| V3 | planned | NPCs (Architect, Designer, Travelers), AI-Town-style map |
| V4 | planned | Three.js 3D town + Temporal for multi-tick build workflows |

## Roadmap

Polis currently lives as a prototype inside the [StudioMeyer Nex-HQ monorepo](https://github.com/studiomeyer-io). Code drop into this repo happens with V2.0. Want to see the V1 code before then? Mail `matthias@studiomeyer.io`.

## Research note

The canonical research and architecture note lives at [meetmyagent.io](https://meetmyagent.io). A cleanly refactored variant of the V1 research report on multi-agent society patterns (Smallville/Voyager/GovSim/AgentVerse/Project Sid) will ship here with V2.0.

## License

MIT (once V2.0 code drops). Until then: concept and roadmap free to reuse with attribution.

---

Built by [Matthias Meyer](https://studiomeyer.io) &middot; [Studio](https://github.com/studiomeyer-io) &middot; 2026
