# Road to AI Engineer

A distilled, organized knowledge base for going from software engineer to **AI
Engineer** — curated roadmaps for Machine Learning, Deep Learning, AI
Engineering, and the Maths for ML, with courses, playlists, and reference
resources split into their own files.

## The roadmap at a glance

> **Where to start:** you can already code but are new to ML → begin at
> **Phase 0** (a quick Python-for-AI refresh) and move top to bottom. Phases are
> numbered **0–5** everywhere in this repo's tracker. The dotted branches are
> optional tracks you can dip into along the way.

```mermaid
flowchart TD
    START(["👋 You can code, new to ML — start here"]) --> P0

    subgraph CORE ["The Core Sequence · do these in order"]
        direction TB
        P0["🐍 Phase 0 · Python for AI<br/>Type hints · asyncio · NumPy / Pandas / Matplotlib · Jupyter<br/><i>~1–2 weeks</i>"]
        P1["📐 Phase 1 · Math Foundations<br/>Stats and probability · linear algebra · calculus · bias-variance<br/><i>~5–7 weeks</i>"]
        P2["🤖 Phase 2 · Classical Machine Learning<br/>Regression · trees · XGBoost · bias-variance · evaluation<br/><i>~8–10 weeks</i>"]
        P3["🧠 Phase 3 · Deep Learning<br/>Backprop · PyTorch · CNNs · Transformers<br/><i>~12–16 weeks</i>"]
        P4["⚡ Phase 4 · Applied AI / LLMs<br/>Tokenization · RAG · fine-tuning · evals<br/><i>~6–8 weeks</i>"]
        P0 --> P1 --> P2 --> P3 --> P4
    end

    P4 --> CAP{{"🚀 Capstone · RAG app on FastAPI, deployed on AWS"}}
    CAP --> HIRED(["🎯 AI Engineer"])

    P5["🕹️ Phase 5 · Agent Engineering and Production<br/>Frameworks · eval harnesses · reliability · deployment<br/><i>~10–15 weeks · optional specialization</i>"]
    CAP -. optional specialization .-> P5

    P1 -. deep dive .-> MFML[/"📊 Maths for ML track"/]
    START -. in a hurry? .-> FAST[/"🏎️ 4-month AI Engineer fast track"/]

    classDef core fill:#0b1f3a,stroke:#22d3ee,stroke-width:2px,color:#e5f6ff;
    classDef track fill:#1e1b3a,stroke:#a78bfa,stroke-width:1px,color:#ede9fe,stroke-dasharray:4 3;
    classDef goal fill:#0f2e1d,stroke:#34d399,stroke-width:2px,color:#d1fae5;
    class P0,P1,P2,P3,P4 core;
    class P5,MFML,FAST track;
    class START,HIRED,CAP goal;
```

**Diagram → files:** Phases 0–4 map to the [Personalised roadmap](roadmaps/personalized-ml-dl-ai/README.md) (its former "Phase 1: Math + Python" is now split into Phase 0 + Phase 1; Phases 2–4 are unchanged) · Phase 5 is the [Agent Engineering](roadmaps/agent-engineering-roadmap.md) track · [Maths for ML](roadmaps/maths-for-ml.md) · [4-month fast track](roadmaps/ai-engineer-roadmap.md). Phase-by-phase tracking lives in the [study tracker](study-tracker/README.md). The fast-track and agent roadmaps keep their own internal "Phase N" numbering; the 0–5 numbers above are the ones to use when tracking progress. At every stage, pull specifics from [courses](courses.md), [playlists](playlists.md), and [resources](resources.md).

## Contents

### 🗺️ Roadmaps
- [Personalised AI + ML + DL Roadmap](roadmaps/personalized-ml-dl-ai/README.md) — the primary phase-by-phase path (Math → Classical ML → Deep Learning → Applied AI). Kept intact.
  - [Phase 0: Python for AI](roadmaps/personalized-ml-dl-ai/phase-0-python-for-ai.md)
  - [Phase 1: Math Foundations](roadmaps/personalized-ml-dl-ai/phase-1-math-foundations.md)
  - [Phase 2: Classical Machine Learning](roadmaps/personalized-ml-dl-ai/phase-2-classical-ml.md)
  - [Phase 3: Deep Learning](roadmaps/personalized-ml-dl-ai/phase-3-deep-learning.md)
  - [Phase 4: Applied AI Engineering / LLM Layer](roadmaps/personalized-ml-dl-ai/phase-4-applied-ai-eng.md)
- [AI Engineer Roadmap (4-Month Fast Track)](roadmaps/ai-engineer-roadmap.md)
- [Agent Engineering Roadmap (~42 Weeks)](roadmaps/agent-engineering-roadmap.md) — the source for Phase 5 (its internal Phase 0–5 numbering is separate)
- [Maths for ML Roadmap](roadmaps/maths-for-ml.md)
- [Full AI Engineering Curriculum (18–24 Months)](roadmaps/full-curriculum-18-24mo.md)
- [Community Study Approaches](roadmaps/community-study-approaches.md) — how experienced people actually studied ML.

### ✅ Study tracker
- [Study Tracker](study-tracker/README.md) — my Phase 0–5 working folder: per-phase notes, exercises, projects, checkpoints, and a daily log.

### 📚 Reference
- [Courses](courses.md) — structured courses, specializations, MIT/Stanford lecture series.
- [Playlists](playlists.md) — topical / creator YouTube playlists.
- [Resources](resources.md) — books, papers, sites, tool docs, repos, blogs, tweets, Reddit, and math platforms.

## How to use this

The recommended learning style here: **treat books as the primary source and
courses as guided demonstrations.** For each phase:

1. Read the book chapter.
2. Watch the corresponding lecture(s) only if a concept isn't clear.
3. Implement the algorithm or model yourself.
4. Build a project.
5. Write a short note or post explaining the concept.

A few principles that recur across the roadmaps:

- **Math is intuition, not proofs** — learn enough to debug and tune, not to derive from scratch.
- **Don't jump to deep learning** — classical ML (regression, trees, the bias-variance trade-off) is the foundation.
- **Depth-wise learning** — build a concrete project and learn what it requires on demand; avoid tutorial hell.
- **Ship in public** — publish projects, write architecture breakdowns; the portfolio is the hiring signal.

## Structure

```
.
├── README.md              ← you are here
├── courses.md
├── playlists.md
├── resources.md
└── roadmaps/
    ├── personalized-ml-dl-ai/   (the primary roadmap, kept intact)
    ├── ai-engineer-roadmap.md
    ├── agent-engineering-roadmap.md
    ├── maths-for-ml.md
    ├── full-curriculum-18-24mo.md
    └── community-study-approaches.md
```
