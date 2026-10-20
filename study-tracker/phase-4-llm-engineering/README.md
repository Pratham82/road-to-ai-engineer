# Phase 4 — LLMs & Applied AI Engineering

**Duration: 6-8 weeks**

## What you're building here

The ability to build production-grade LLM applications — not just call an API and hope, but reason about tokenization costs, why a RAG pipeline is retrieving garbage, when fine-tuning beats prompting, and how to measure whether any of it actually works. This is the phase that turns "did the DL coursework" into "AI Engineer" in the job-title sense — and where your existing frontend/backend/AWS/API skills merge back in and become an edge.

## Topics, in order

**1. Tokenization & embeddings**
- Byte-Pair Encoding — how text becomes tokens, why token count ≠ word count (cost + context-window math)
- Embeddings: what they represent geometrically ("king - man + woman ≈ queen")
- Context windows — what exceeding one actually does, why longer isn't always better

**2. Inference mechanics**
- Sampling: temperature, top-k, top-p — what each actually changes about output
- KV caching — why this makes autoregressive generation fast, conceptually
- This layer is why API parameters behave the way they do, instead of tweaking them by feel

**3. Fine-tuning approaches**
- Full fine-tuning vs. parameter-efficient methods (LoRA, QLoRA)
- When fine-tuning actually beats prompting — a judgment call, not a default

**4. Retrieval-Augmented Generation (RAG)**
- Vector databases: Pinecone, Chroma, Weaviate, pgvector — how similarity search works underneath; these are "memory" for the AI, not just databases
- Chunking strategies, embedding choice, retrieval quality — where most real RAG systems actually break, and where Phase 3's embedding-geometry intuition pays rent
- End-to-end architecture: ingest → chunk → embed → store → retrieve → generate

**5. Evaluation**
- How to measure whether an LLM app actually works — not vibes-based judgment
- Basic eval frameworks: relevance, faithfulness, answer correctness against a labeled set (RAGAS, Arize Phoenix, LangSmith, Braintrust)

**6. Orchestration & agent basics** (lighter touch here — full depth is Phase 5)
- Prompt patterns: few-shot, chain-of-thought, forcing structured/JSON output
- Tool calling, basic agent loops — enough to know what LangChain/LangGraph/LlamaIndex are doing under the abstraction

## Courses & books

See [Curated Resources → Phase 4](../docs/curated-resources.md#phase-4--llms--applied-ai-engineering).

## Capstone project — the one that actually matters for job applications

**Build a RAG application on your own FastAPI backend, deployed on AWS**, with real evaluation:

- FastAPI backend exposing endpoints for document ingestion and querying
- Vector DB (Chroma is a good free starting point) for storage/retrieval
- An actual evaluation set — even 20-30 labeled Q/A pairs — so you can say "retrieval precision improved from X to Y after changing chunking strategy," not "it seems to work better"
- Deploy on AWS — dual-purpose with AWS cert prep if that's active

This single project is the strongest portfolio artifact for AI Engineer roles: it demonstrates frontend/backend fluency, cloud deployment, and genuine DL understanding underneath the RAG mechanics, in a way no certificate can.

## Checkpoint before moving to Phase 5

See [CHECKPOINT.md](CHECKPOINT.md).
