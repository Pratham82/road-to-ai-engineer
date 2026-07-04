# Full AI Engineering Curriculum (18–24 Months)

> A university-degree-style curriculum instead of random overlapping courses.
> Every phase has: one primary book (theory), one primary course
> (implementation), projects, and optional references.
>
> Books, courses, and papers referenced here are collected in
> [`../courses.md`](../courses.md) and [`../resources.md`](../resources.md).

The biggest problem with taking random courses from different creators is overlap — you end up watching 300+ hours of repeated material. Build a **curriculum** instead.

---

## Phase 0 — Python for AI (2 Weeks)

**Goal:** Refresh Python specifically for AI and data science.
**Topics:** Advanced Python, type hints, iterators, generators, decorators, context managers, dataclasses, virtual environments, packaging.
**Books:** Python Tricks · Effective Python
**Courses:** Python for Everybody (skim advanced sections) · Complete Python Bootcamp (reference only)
**Libraries:** NumPy · Pandas · Matplotlib · SciPy · Jupyter

## Phase 1 — Mathematics (2–3 Months)

This is the most important phase. See also the dedicated [Maths for ML roadmap](maths-for-ml.md).

- **Linear Algebra** — vectors, matrices, dot product, eigenvalues, eigenvectors, SVD.
    - Books: Mathematics for Machine Learning ⭐ · Introduction to Linear Algebra
    - Courses: Essence of Linear Algebra ⭐⭐⭐⭐⭐ · MIT 18.06 Linear Algebra
- **Calculus**
    - Books: Mathematics for Machine Learning · Calculus (reference only)
    - Courses: Essence of Calculus
- **Probability & Statistics**
    - Books: Think Stats · Mathematics for Machine Learning
    - Courses: Khan Academy Statistics and Probability

## Phase 2 — Data Analysis (1 Month)

**Topics:** Pandas, NumPy, EDA, feature engineering, visualization.
**Book:** Python for Data Analysis ⭐⭐⭐⭐⭐
**Course:** Data Analysis with Python

## Phase 3 — Machine Learning (3 Months)

**Framework:** scikit-learn
**Books:** Hands-On Machine Learning ⭐ (primary) · An Introduction to Statistical Learning (free) · Pattern Recognition and Machine Learning (advanced)
**Courses:** Machine Learning Specialization ⭐⭐⭐⭐⭐ · CS229 (optional, advanced)
**Projects:** House Price Prediction · Spam Detection · Recommendation Engine · Fraud Detection

## Phase 4 — Deep Learning (3 Months)

**Framework:** PyTorch
**Books:** Dive into Deep Learning ⭐ (free) · Deep Learning ⭐⭐⭐⭐⭐
**Courses:** Practical Deep Learning for Coders ⭐⭐⭐⭐⭐ · Deep Learning Specialization (advanced)
**Projects:** MNIST · CIFAR-10 · Image Classifier

## Phase 5 — Computer Vision (2 Months)

**Book:** Deep Learning for Vision Systems
**Course:** CS231n ⭐⭐⭐⭐⭐
**Projects:** OCR · Object Detection · Face Recognition

## Phase 6 — NLP (2 Months)

**Book:** Speech and Language Processing ⭐⭐⭐⭐⭐
**Course:** CS224N
**Projects:** Sentiment Analysis · Chatbot · Text Classification

## Phase 7 — Transformers (2 Months)

**Book:** Natural Language Processing with Transformers ⭐
**Papers:** Attention Is All You Need — read thoroughly, implement from scratch.
**Course:** Hugging Face NLP Course ⭐⭐⭐⭐⭐

## Phase 8 — Large Language Models (2 Months)

**Topics:** GPT · BERT · LoRA · RLHF · DPO · Quantization
**Book:** Build a Large Language Model (From Scratch) ⭐⭐⭐⭐⭐ (no definitive LLM textbook exists yet)
**Courses:** Full Stack Deep Learning · Hugging Face NLP Course
**Projects:** Fine-tune a model · RAG chatbot

## Phase 9 — AI Engineering (2 Months)

**Topics:** RAG · Agents · Tool Calling · MCP · Context Engineering · Evaluation · Guardrails
**Books:** No single comprehensive book yet — read documentation and architecture guides.
**Frameworks:** LangChain · LlamaIndex
**Courses:** LangChain for LLM Application Development · Building Systems with the ChatGPT API
**Projects:** AI Coding Assistant · PDF Chat · AI Research Agent

## Phase 10 — MLOps (1 Month)

**Book:** Designing Machine Learning Systems ⭐⭐⭐⭐⭐
**Course:** Made With ML
**Tools:** MLflow · Weights & Biases

## Phase 11 — AI Infrastructure (1 Month)

**Topics:** CUDA basics · GPUs · Distributed Training · Quantization · ONNX · TensorRT concepts
**Book:** CUDA by Example (optional, for infrastructure roles)

## Phase 12 — Research (Ongoing)

Read papers weekly. Start with: Attention Is All You Need · BERT · Language Models are Few-Shot Learners · LoRA: Low-Rank Adaptation of Large Language Models.

---

## The "Core Six" Resources to Prioritize

| Area | Resource |
|---|---|
| Mathematics | _Mathematics for Machine Learning_ |
| Machine Learning | _Hands-On Machine Learning with Scikit-Learn, Keras, and TensorFlow_ |
| Deep Learning | _Dive into Deep Learning_ |
| LLMs | _Build a Large Language Model (From Scratch)_ |
| MLOps | _Designing Machine Learning Systems_ |
| Transformers | _Attention Is All You Need_ paper |

These six, combined with implementing projects and reading official docs, provide a strong foundation without dozens of overlapping materials.

## One recommendation for this learning style

Given a preference for structured roadmaps, deep understanding, and building over passive watching: **treat books as the primary source of learning and courses as guided demonstrations.** For each phase:

1. Read the book chapter.
2. Watch the corresponding lecture(s) only if a concept isn't clear.
3. Implement the algorithm or model yourself.
4. Build a project.
5. Write a short note or LinkedIn post explaining the concept.
