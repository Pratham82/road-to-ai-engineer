# Personalised AI + ML + DL Roadmap

> Based on the original personalized roadmap, renumbered to Phases 0–5 (Python split
> out as Phase 0; Agent Engineering added as optional Phase 5). This is the primary,
> phase-by-phase learning path. Each phase links to its own detailed breakdown.

Here's the full roadmap with a **Recommended Books** section added to each phase, so you can pair reading with the courses.

## The core sequence

```
Python for AI → Math Foundations → Classical ML → Deep Learning → Applied AI Engineering (LLM layer)
                                                                          ↳ (optional) Agent Engineering
```

Phases are numbered **0–5**. The original "Math + Python Foundations" phase is now split into Phase 0 (Python for AI) and Phase 1 (Math Foundations).

---

## [Phase 0: Python for AI](phase-0-python-for-ai.md)

**Duration: 1-2 weeks** (refresh only)

**What to learn:** Type hints, generators, decorators, dataclasses, virtual envs and packaging (Poetry/Rye), asyncio and JSON/tool-calling patterns, NumPy/Pandas/Matplotlib, Jupyter.

**Courses:**

- Python for Everybody (skim advanced sections only)

**Books (reference):**

- _Python Tricks_, _Effective Python_

**Checkpoint**: Comfortable in Jupyter, can explain what vectorization replaces, virtual env + packaging second-nature.

---

## [Phase 1: Math Foundations](phase-1-math-foundations.md)

**Duration: 5-7 weeks**

**What to learn:** Statistics and probability first, then linear algebra, calculus (derivatives, chain rule), and ML-specific math (loss functions, gradient descent, bias-variance).

**Courses:**

- 3Blue1Brown — "Essence of Linear Algebra" + "Essence of Calculus" (YouTube, free)
- Khan Academy — Statistics & Probability, Linear Algebra, Calculus (free)
- Mathematics for Machine Learning Specialization (Imperial College London, Coursera)
- An Introduction to Statistical Learning (ISLR) — free book + YouTube series
- Kaggle micro-courses — "Pandas," "Intro to Machine Learning" (free)

**Books:**

- **Mathematics for Machine Learning** by Deisenroth, Faisal, Ong — widely considered the modern gold standard for beginners and intermediates, explicitly designed to bridge traditional math textbooks and practical programming, with the first half covering pure math and the second half showing how those concepts power algorithms like SVMs and PCA. Free PDF available (mml-book.com). Pair this directly with the Imperial College course — they cover the same ground.
- **Linear Algebra and Its Applications** by Gilbert Strang (optional, if you want the deeper university-level version) — Strang's approach is described as a masterclass in mathematical thinking that has shaped a generation of ML practitioners, with particular strength in SVD, eigendecomposition, and topics that show up constantly in ML papers.

**Checkpoint project**: Full EDA on a real dataset in Pandas.

---

## [Phase 2: Classical Machine Learning](phase-2-classical-ml.md)

**Duration: 8-10 weeks**

**What to learn:** Regression, classification, decision trees, random forests, XGBoost, bias-variance tradeoff, regularization, cross-validation, evaluation metrics.

**Courses:**

- Machine Learning Specialization (Andrew Ng, DeepLearning.AI, Coursera)
- StatQuest with Josh Starmer (YouTube, free)

**Books:**

- **Hands-On Machine Learning with Scikit-Learn, Keras, and TensorFlow** by Aurélien Géron — a practical guide to building ML systems in Python, not a theory book, covering the full pipeline: data cleaning, feature engineering, model training, evaluation, and deployment basics. This is the book to run alongside Ng's course — code-heavy, matches how you already like to learn.
- **An Introduction to Statistical Learning (ISLR)** by James, Witten, Hastie, Tibshirani — still relevant for foundations like the bias-variance trade-off, cross-validation, regularization, and model selection, though it doesn't cover deep learning or anything post-2015. Free PDF at ISLR.org, with Python labs added recently. Read this once Géron's practical explanations start feeling thin on the "why."

**Project**: 2-3 Kaggle competitions, full pipeline.

---

## [Phase 3: Deep Learning](phase-3-deep-learning.md)

**Duration: 12-16 weeks**

**What to learn:** NN fundamentals, backprop, CNNs (compressed), transformers/attention — the centerpiece phase.

**Courses:**

- Practical Deep Learning for Coders (fast.ai, free)
- Deep Learning Specialization (Andrew Ng, DeepLearning.AI) — supplementary
- Neural Networks: Zero to Hero (Andrej Karpathy, YouTube, free)
- The Illustrated Transformer (Jay Alammar, blog, free)

**Books:**

- **Deep Learning** by Goodfellow, Bengio, Courville — often called the "Bible of Deep Learning," written by pioneers of the field, contextualizing the math within deep learning and showing exactly why each formula matters, though it reads more like a university reference manual than a beginner tutorial. Part 1 specifically ("Applied Math and Machine Learning Basics") is considered one of the best mathematical crash courses available anywhere — read that part as a bridge from Phase 1, then dip into later chapters as reference rather than cover-to-cover.
- **Dive into Deep Learning (d2l.ai)** — free, code-first, interactive book with runnable notebooks alongside every concept; pairs naturally with fast.ai's style and covers transformers in depth.

**Reading**: "Attention Is All You Need" (original paper) — after Illustrated Transformer + Karpathy.

**Projects**: Backprop from scratch (NumPy) → PyTorch rebuild → Karpathy's GPT-from-scratch, extended.

---

## [Phase 4: Applied AI Engineering / LLM Layer](phase-4-applied-ai-eng.md)

**Duration: 6-8 weeks**

**What to learn:** Tokenization, embeddings, RAG, fine-tuning (LoRA/QLoRA), evaluation.

**Courses:**

- DeepLearning.AI short courses (LangChain, RAG, Finetuning LLMs)
- Hugging Face NLP Course (free)
- Full Stack LLM Bootcamp (free lectures)

**Books:**

- **Natural Language Processing with Transformers** by Tunstall, von Werra, Wolf (O'Reilly, written by Hugging Face engineers) — the closest thing to an industry-standard book for this exact phase; walks through tokenization, fine-tuning, and deployment using the actual Hugging Face stack you'll use in the course.
- **Designing Machine Learning Systems** by Chip Huyen — less about model internals, more about production ML/LLM systems: data pipelines, evaluation, deployment, monitoring. Directly relevant to your capstone RAG project since it covers the "shipping it for real" concerns most courses skip.

**Capstone project**: RAG application on your own FastAPI backend, deployed on AWS.

---

## [Phase 5: Agent Engineering & Production](../agent-engineering-roadmap.md) (optional specialization)

**Duration: ~10-15 weeks**

**What to learn:** Agent frameworks and workflows (LangGraph, CrewAI, AutoGen), eval harnesses and agent infrastructure, production reliability (observability, fallbacks, CI eval gates, prompt-injection defense), deployment hardening (Docker, queues, Redis, caching).

**Builds, in order:** tool-using assistant → RAG chatbot (extend the Phase 4 capstone) → Research Analyst Agent → evaluation harness (~1,500 LOC) → production-ready agent.

Pursue this if the target role leans "Agent/AI Engineer" rather than "ML Engineer". The detailed week-by-week plan is the [Agent Engineering Roadmap](../agent-engineering-roadmap.md), which keeps its own internal Phase 0-5 numbering.

---

## Full timeline

|Phase|Duration|Primary Course|Primary Book|
|---|---|---|---|
|0: Python for AI|1-2 wks|Python for Everybody (skim)|Effective Python (reference)|
|1: Math Foundations|5-7 wks|Math for ML Specialization|Mathematics for Machine Learning (Deisenroth et al.)|
|2: Classical ML|8-10 wks|ML Specialization (Ng)|Hands-On Machine Learning (Géron)|
|3: Deep Learning|12-16 wks|fast.ai + Karpathy's Zero to Hero|Deep Learning (Goodfellow et al.), Part 1 + reference|
|4: Applied AI Eng|6-8 wks|DeepLearning.AI + HF NLP Course|NLP with Transformers (Tunstall et al.)|
|5: Agent Eng (optional)|10-15 wks|See Agent Engineering Roadmap|Designing Machine Learning Systems (Huyen)|

**Total (Phases 0-4): ~32-43 weeks (7.5-10 months)**; with optional Phase 5: ~42-58 weeks

One caution worth flagging plainly: most formal courses like fast.ai and Andrew Ng's sequence are already self-contained — the risk with adding books is spreading attention too thin rather than going deeper. I'd treat the books as **reference material to dip into when a course concept feels thin**, not as a second syllabus to read cover-to-cover in parallel. Géron's book especially can mostly replace re-reading course transcripts.
