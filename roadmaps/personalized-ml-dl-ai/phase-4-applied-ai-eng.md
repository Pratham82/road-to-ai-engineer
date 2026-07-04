# Phase 4: Applied AI Engineering / LLM Layer

Here's the full breakdown of Phase 4 — where everything from Phases 1-3 finally turns into something you can ship, and where your existing frontend/backend/AWS skills merge back in.

## What you're building here

The ability to build production-grade LLM applications — not just call an API and hope, but actually reason about tokenization costs, why a RAG pipeline is retrieving garbage, when fine-tuning beats prompting, and how to measure whether any of it is actually working. This is the phase that turns you from "did the DL coursework" into "AI Engineer" in the job-title sense.

## Topics, in order

**1. Tokenization & embeddings**

- Byte-Pair Encoding (BPE) — how text actually becomes tokens, and why token count ≠ word count (matters for cost and context window math)
- Embeddings: what they represent geometrically, why "king - man + woman ≈ queen" works
- Context windows — what's actually happening when you exceed one, and why longer isn't always better

**2. Inference mechanics**

- Sampling: temperature, top-k, top-p — and what each one actually changes about output
- KV caching — why this makes autoregressive generation fast, conceptually
- This layer explains _why_ certain API parameters behave the way they do, instead of just tweaking them by feel

**3. Fine-tuning approaches**

- Full fine-tuning vs parameter-efficient methods (LoRA, QLoRA)
- When fine-tuning actually beats prompting (this is a judgment call worth understanding properly, not just "fine-tune when in doubt")

**4. Retrieval-Augmented Generation (RAG)**

- Vector databases: Pinecone, Chroma, Weaviate — how similarity search actually works underneath
- Chunking strategies, embedding choice, retrieval quality — this is where most real-world RAG systems actually break, and where your DL foundations (embeddings geometry) pay rent
- End-to-end RAG architecture: ingest → chunk → embed → store → retrieve → generate

**5. Evaluation**

- How to measure whether an LLM app is actually working — not vibes-based judgment
- Basic eval frameworks: relevance, faithfulness, answer correctness against a labeled set

**6. Agent basics** (lighter touch, but worth knowing)

- Tool calling, basic agent loops — enough to know what LangChain/LlamaIndex are actually doing under the abstraction

## Courses

- **DeepLearning.AI short courses** — specifically: "LangChain for LLM Application Development," "Building and Evaluating Advanced RAG," "Finetuning Large Language Models." These are short (hours, not weeks) but built directly with the companies whose tools you'll use (OpenAI, LangChain), so they stay current.
- **Hugging Face NLP Course** (free, huggingface.co) — the industry-standard practical resource for tokenization, fine-tuning, and the Transformers library itself. Very hands-on, code-first.
- **Full Stack LLM Bootcamp** (Full Stack Deep Learning, free lecture content) — fills the gap the above courses skip: how to actually deploy, monitor, and evaluate LLM systems in production, built by practitioners rather than researchers.

## Books

- **Natural Language Processing with Transformers** by Tunstall, von Werra, Wolf (O'Reilly, written by Hugging Face engineers) — closest thing to an industry-standard book for this exact phase. Walks through tokenization, fine-tuning, and deployment using the same Hugging Face stack you'll use in the course above, so the book and course reinforce each other directly.
- **Designing Machine Learning Systems** by Chip Huyen — less about model internals, more about production concerns: data pipelines, evaluation, deployment, monitoring, feedback loops. Directly relevant to your capstone project since it covers the "shipping it for real" problems that pure ML/DL courses skip entirely.

## Suggested weekly rhythm (at 8-10 hrs/week)

- 2-3 hrs: Hugging Face NLP Course modules
- 2-3 hrs: DeepLearning.AI short courses (these move fast, expect to finish each in 1-2 weeks)
- 1-2 hrs: NLP with Transformers book, alongside whatever the HF course covers that week
- 2-3 hrs: capstone project build time

## Capstone project — this is the one that actually matters for job applications

**Build a RAG application on your own FastAPI backend, deployed on AWS**, with real evaluation (not vibes). Concretely:

- FastAPI backend (you already have this foundation) exposing endpoints for document ingestion and querying
- Vector DB (Chroma is a good free starting point) for storage/retrieval
- An actual evaluation set — even 20-30 labeled question/answer pairs — so you can say "retrieval precision improved from X to Y after I changed chunking strategy" instead of "it seems to work better"
- Deploy it on AWS (this also reinforces your DVA-C02 cert prep — genuinely dual-purpose time)

This single project is the strongest artifact in your entire portfolio for AI Engineer roles, because it demonstrates the full stack — frontend/backend fluency, cloud deployment, and genuine DL understanding underneath the RAG mechanics — in a way no certificate can.

## Checkpoint — you're done with the roadmap when

- You can explain why a RAG pipeline is retrieving irrelevant chunks and fix it (chunking, embedding model choice, or retrieval strategy — not just "add more documents")
- You can justify choosing fine-tuning vs. prompting vs. RAG for a given problem, not just default to whichever is trendy
- You can set up a basic eval loop for an LLM app and explain what the numbers mean
- Your capstone project is live, deployed, and something you could walk an interviewer through end-to-end

At this point you'd have the full stack: math foundations, classical ML instincts, real DL understanding of transformers, and the applied layer that turns it into shippable product work — genuinely differentiated from the wrapper-only AI engineer crowd you were originally trying to avoid becoming.
