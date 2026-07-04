# AI Engineer Roadmap (4-Month Fast Track)

> A compressed, senior-engineer-oriented path into AI Engineering. Assumes you
> already have strong software fundamentals and want to focus on the "data
> mindset" and the LLM application layer rather than syntax.
>
> Courses and books referenced here live in [`../courses.md`](../courses.md) and
> [`../resources.md`](../resources.md).

Related: [roadmap.sh AI Engineer track](https://roadmap.sh/ai-engineer) · [AI-Study-Group](https://github.com/ArturoNereu/AI-Study-Group)

---

## Phase 1: The Foundations (Month 1)

_Since you're already a Senior Engineer, focus on the "Data Mindset" rather than just syntax._

- **Python for Engineers:** Learn Python deeply. Focus on **Type Hinting**, **AsyncIO**, and **Package Management** (Poetry or Rye). You'll find it feels like a stricter, cleaner version of TypeScript.
- **The Math "Core":** Don't get stuck in a PhD. Learn:
    - **Linear Algebra:** Understanding how data is represented as Vectors and Matrices.
    - **Statistics:** Mean, standard deviation, and probability (needed to understand model "confidence").
- **The Big Three Libraries:**
    - **NumPy:** For high-speed math.
    - **Pandas/Polars:** For manipulating data tables (like an Excel sheet in code).
    - **PyTorch:** Learn the basics of "Tensors" (the data structure AI uses).

---

## Phase 2: Generative AI & LLM Orchestration (Month 2)

_This is where your frontend skills (API integration) give you an edge._

- **API Mastery:** Move beyond simple Chat prompts. Learn to use **OpenAI/Anthropic APIs** programmatically (managing system prompts, temperature, and tokens).
- **Prompt Engineering Patterns:** Learn **Few-shot prompting**, **Chain-of-Thought**, and **Output Parsing** (forcing a model to return valid JSON for your frontend).
- **LangChain / LangGraph:** These are the "React" of AI. They help you build complex chains of logic (e.g., "If user asks X, search the database; if they ask Y, look at the web").
- **Vector Databases:** Learn **Pinecone** or **pgvector**. Understand that these aren't just databases; they are "Memory" for your AI.

---

## Phase 3: RAG & Agentic Systems (Month 3)

_Retrieval-Augmented Generation (RAG) is the most in-demand industry skill right now._

- **RAG Architecture:** Build a system where an AI can "read" your private PDF or GitHub repo.
    - Learn **Chunking** (breaking text into pieces) and **Embeddings** (turning text into numbers).
- **AI Agents:** Build "Agentic" workflows using **CrewAI** or **AutoGPT**. These are systems that can take a goal (e.g., "Research this company and write a summary") and perform multiple steps autonomously.
- **Evaluation:** How do you know your AI is good? Learn **RAGAS** or **Arize Phoenix** to measure hallucinations and accuracy.

---

## Phase 4: MLOps & Deployment (Month 4)

_Bridge the gap between a "cool demo" and a "stable product."_

- **Serving Models:** Learn **FastAPI** to build high-performance Python backends for your AI features.
- **Deployment:** Learn how to deploy AI apps using **Docker** and cloud services like **AWS Bedrock** or **Vercel AI SDK**.
- **Observability:** Implement **LangSmith** or **Weights & Biases** to track how your AI is performing in the real world.

---

## How to Study (The Senior Engineer's Way)

Don't just watch videos. Use your frontend skills to build as you go:

1. **Read Chip Huyen's _AI Engineering_** to understand the big picture.
2. **Take Andrew Ng's _Machine Learning Specialization_** to get the math "aha!" moments.
3. **Build a Project:** Take your current knowledge of React/Next.js and build an **AI-powered Code Reviewer**. Use a Python (FastAPI) backend, PyTorch for local processing, and OpenAI/Anthropic APIs for the heavy lifting.
