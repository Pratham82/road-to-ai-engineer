# Phase 5 — Agent Engineering & Production

**Duration: ~10-15 weeks** (optional specialization — pursue if the target role leans "Agent/AI Engineer" rather than "ML Engineer")

## What you're building here

Everything past Phase 4's basics: multi-step orchestration, evaluation harnesses, and the production-reliability thinking companies actually screen for now. The original source material for this phase ("agent-roadmap-2026") frames it around hiring — the deliverables below are explicitly portfolio-shaped.

## Topics, in order

**1. Agent frameworks & workflows**
- LangGraph, CrewAI, AutoGen concepts
- Multi-step orchestration, planning/execution loops, retries/checkpoints
- Tracing, observability, prompt debugging (LangSmith, OpenTelemetry basics)

**2. Agent infrastructure & harnesses** — this is what differentiates from "tutorial engineer"
- Eval harnesses, benchmark testing, replay systems, prompt regression testing, dataset generation

**3. Production AI engineering** — the phase that matters most for getting hired
- Reliability, observability, production debugging, latency optimization, prompt-injection defense, cost optimization
- Fallback models, retries, logging, analytics, CI evaluation gates

**4. Deployment & hardening**
- Docker, queues, Redis, async systems, background jobs, caching, token optimization, rate-limit handling

## Build, in order

1. **Tool-using assistant** — web search tool, calculator tool, file reader, memory, streaming UI
2. **RAG chatbot** — embeddings, chunking, retrieval, citations, conversation history (overlaps with Phase 4 capstone — extend rather than rebuild)
3. **Research Analyst Agent** — search, summarize, cite sources, generate reports, save memory; capture LangSmith traces
4. **Evaluation harness (~1,500 LOC target)** — run prompts against datasets, compare outputs, score responses, store metrics, track failures; ship with a post-mortem writeup
5. **Production-ready agent** — monitoring, retries, fallback models, logging, analytics, CI evaluation gate

Publish every project on GitHub with an architecture breakdown, screenshots/demo GIFs — this phase is explicitly about building a public, hireable trail, not just learning.

## Courses & resources

See [Curated Resources → Phase 5](../docs/curated-resources.md#phase-5--agent-engineering--production).

## Interview positioning (carried over from the original plan — still holds)

> "Frontend engineer transitioning into AI product engineering with strong UX + production engineering experience" beats "I watched agent tutorials." Lead with React/Next.js background, API experience, product thinking, and frontend architecture skills — AI companies increasingly need engineers who can ship usable AI products, not just prototype prompts.

## Checkpoint — roadmap complete when

See [CHECKPOINT.md](CHECKPOINT.md).
