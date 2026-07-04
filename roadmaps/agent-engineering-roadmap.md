# Agent Engineering Roadmap (~42 Weeks)

> Personalized from [agent-roadmap-2026](https://github.com/codejunkie99/agent-roadmap-2026) on May 7, 2026.
> A zero-to-hired path for building AI agents, tuned for a frontend engineer
> transitioning into AI product engineering.
>
> Tool docs and resources referenced here live in [`../resources.md`](../resources.md).

## Profile

- **Level:** Never built an agent
- **Time:** ~5 hrs/week
- **Stack:** Python + OpenAI
- **Goal:** Get hired as an AI/Agent Engineer
- **Total estimated duration:** ~42 weeks

---

## Before You Start

Since you're starting from zero with AI agents, spend 1–2 weeks first getting comfortable with:

- Python basics for AI workflows
- APIs
- async concepts
- JSON/tool calling
- embeddings

**Recommended prerequisite:** [Hugging Face LLM Course](https://huggingface.co/learn/llm-course)

Do not try to master ML theory first. Focus on: **building applications using models.**

---

## Phase 0 — Mental Models (2.5 weeks)

Because you're new to agents, this phase is important for understanding: agents vs workflows, RAG, memory, tools, evals, orchestration.

**Learn:** LLM lifecycle · Tool calling · RAG pipelines · Context windows · Agent loops · Planning vs execution · Memory systems · Prompt engineering fundamentals

**Deliverable:** Write a 2-page "How AI Agents Work" document in your own words.

---

## Phase 1 — Foundation Agent Engineering (7.5 weeks)

Since you're using OpenAI, use the OpenAI Agents SDK instead of Claude SDK.

**Focus:** OpenAI SDK · OpenAI Agents SDK · structured outputs · function calling · streaming · embeddings · vector databases · RAG

**Build:**

- **Project 1 — Tool-Using Assistant:** web search tool, calculator tool, file reader, memory, streaming UI.
- **Project 2 — RAG Chatbot:** embeddings, chunking, retrieval, citations, conversation history.

**Important caveat:** The OpenAI Agents SDK is productive but somewhat OpenAI-locked. Later phases should expose you to broader orchestration patterns.

**Public portfolio requirement:** publish every project on GitHub, write a short architecture breakdown, add screenshots + demo GIFs.

---

## Phase 2 — Agent Frameworks + Workflows (10 weeks)

**Learn:** LangGraph · CrewAI · AutoGen concepts · multi-step orchestration · planning/execution loops · retries/checkpoints

**Build — Research Analyst Agent:** search, summarize, cite sources, generate reports, save memory.

**Required skills:** tracing · observability · prompt debugging · evaluation basics
**Strongly recommended:** LangSmith · OpenTelemetry basics

**Hiring signal:** architecture diagrams, trace screenshots, failure analysis writeups. These matter heavily in interviews now.

---

## Phase 3 — Agent Infrastructure + Harnesses (10 weeks)

This is where you start differentiating yourself from tutorial engineers.

**Learn:** eval harnesses · benchmark testing · replay systems · prompt regression testing · dataset generation

**Build — Mini Evaluation Harness (~1,500 LOC target):** run prompts against datasets, compare outputs, score responses, store metrics, track failures.

**Deliverables:** Post-mortem document · Evaluation datasets · Benchmark runs · Architecture notes
**Public requirement:** GitHub repo · technical writeup · demo video

---

## Phase 4 — Production AI Engineering (7.5 weeks)

This phase is the most important for getting hired.

**Focus areas:** evals · reliability · observability · production debugging · latency optimization · prompt safety · cost optimization

**Learn:** LangSmith · Braintrust · OpenAI evals · tracing systems · prompt injection defense

**Build — Production-Ready Agent:** monitoring, retries, fallback models, logging, analytics, CI evaluation gate.

**Most important hiring signal:** reliability thinking · evaluation methodology · debugging maturity. Companies care more about this now than fancy multi-agent demos.

---

## Phase 5 — Production Hardening + Career Layer (5 weeks)

**Learn:** deployment · Docker · queues · Redis · async systems · background jobs · cost discipline · caching

**Deliverables:** production hardening checklist · deployment architecture · rate limit handling · token optimization

**Career focus:** polish GitHub · write blogs · post architecture breakdowns · share learnings publicly · apply to AI engineering roles

---

## Project Deliverables Checklist

- [ ] Phase 0: 2-page mental-model document
- [ ] Phase 1: Tool-using OpenAI Agent SDK assistant
- [ ] Phase 1: Production-style RAG chatbot
- [ ] Phase 2: Research Analyst Agent + LangSmith traces
- [ ] Phase 3: 1,500-line evaluation harness + post-mortem
- [ ] Phase 4: Golden dataset + CI eval gate + benchmark run
- [ ] Phase 5: Production hardening checklist
- [ ] Publish one public GitHub project per phase
- [ ] Publish one technical writeup per phase

---

## Interview Positioning Strategy

Your strongest positioning is:

> "Frontend engineer transitioning into AI product engineering with strong UX + production engineering experience."

That is significantly more valuable than "I watched agent tutorials." Leverage your React/Next.js background, API experience, product thinking, and frontend architecture skills. AI companies increasingly need engineers who can build usable AI products, not just prototype prompts.

---

## Next Action

1. Complete the first 3 chapters of the [Hugging Face LLM Course](https://huggingface.co/learn/llm-course).
2. Set up a dedicated GitHub repo called `agent-engineering-roadmap`.
3. Build a minimal Python OpenAI chat CLI with streaming responses.
