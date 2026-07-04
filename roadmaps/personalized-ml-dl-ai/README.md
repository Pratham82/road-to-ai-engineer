# Personalised AI + ML + DL Roadmap

> Kept as-is from the original personalized roadmap. This is the primary,
> phase-by-phase learning path. Each phase links to its own detailed breakdown.

Here's the full roadmap with a **Recommended Books** section added to each phase, so you can pair reading with the courses.

## The core sequence

```
Math/Python Foundations → Classical ML → Deep Learning → Applied AI Engineering (LLM layer)
```

---

## [Phase 1: Math + Python Foundations](phase-1-math-python.md)

**Duration: 5-7 weeks**

**What to learn:** Linear algebra, calculus (derivatives, chain rule), probability/stats, NumPy + Pandas fluency.

**Courses:**

- 3Blue1Brown — "Essence of Linear Algebra" + "Essence of Calculus" (YouTube, free)
- Mathematics for Machine Learning Specialization (Imperial College London, Coursera)
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

## Full timeline

|Phase|Duration|Primary Course|Primary Book|
|---|---|---|---|
|1: Math/Python|5-7 wks|Math for ML Specialization|Mathematics for Machine Learning (Deisenroth et al.)|
|2: Classical ML|8-10 wks|ML Specialization (Ng)|Hands-On Machine Learning (Géron)|
|3: Deep Learning|12-16 wks|fast.ai + Karpathy's Zero to Hero|Deep Learning (Goodfellow et al.), Part 1 + reference|
|4: Applied AI Eng|6-8 wks|DeepLearning.AI + HF NLP Course|NLP with Transformers (Tunstall et al.)|

**Total: ~31-41 weeks (7-10 months)**

One caution worth flagging plainly: most formal courses like fast.ai and Andrew Ng's sequence are already self-contained — the risk with adding books is spreading attention too thin rather than going deeper. I'd treat the books as **reference material to dip into when a course concept feels thin**, not as a second syllabus to read cover-to-cover in parallel. Géron's book especially can mostly replace re-reading course transcripts.
