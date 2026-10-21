# Curated Resources (Books, Courses, Playlists, Links)

One list, deduplicated from six overlapping source files. Grouped by phase; each phase has a **primary** book + course (do these) and **optional/reference** (dip into only when a concept feels thin).

## Phase 0 — Python for AI

- **Course:** Python for Everybody (skim advanced sections only)
- **Books (reference):** *Python Tricks*, *Effective Python*
- **Libraries to get comfortable with:** NumPy, Pandas, Matplotlib, SciPy, Jupyter

## Phase 1 — Math Foundations

**Primary path, in order:**
1. 3Blue1Brown — *Essence of Linear Algebra* + *Essence of Calculus* (YouTube, free) — visual intuition first, ~5-6 hrs combined. [Essence of Linear Algebra playlist](https://www.youtube.com/playlist?list=PLZHQObOWTQDPD3MizzM2xVFitgF8hE_ab)
2. Khan Academy — Statistics & Probability (free, ~50 hrs) → Linear Algebra (1-2 wks) → Calculus (1-2 wks)
3. **Mathematics for Machine Learning Specialization** (Imperial College London, Coursera) — turns the 3Blue1Brown intuition into formal, ML-framed working knowledge. [Linear Algebra module on YouTube](https://www.youtube.com/playlist?list=PLiiljHvN6z1_o1ztXTKWPrShrMrBLo5P3)
4. **"An Introduction to Statistical Learning" (ISLR)** — free at [statlearning.com](https://www.statlearning.com/), or the authors' free YouTube series — connects the math to real ML techniques

**Primary book:** *Mathematics for Machine Learning* by Deisenroth, Faisal, Ong — free PDF at mml-book.com. Gold-standard bridge from pure math to the algorithms (SVM, PCA) that use it. Use as a companion to the Imperial College course, not a second syllabus.

**Optional/reference:** *Linear Algebra and Its Applications* (Gilbert Strang) — deeper, university-level, strong on SVD/eigendecomposition. MIT OCW 18.06 Linear Algebra / 18.01 Calculus if you want MIT's actual course materials. Paul's Online Math Notes for solved-problem practice. *Think Stats* and *Practical Statistics for Data Science* as stats-specific alternates.

**If you ever need a paid structured platform:** Math Academy (adaptive, practice-only) — free equivalents are Khan Academy (video+practice) or Mathigon (interactive, free).

## Phase 2 — Classical ML

**Primary course:** Machine Learning Specialization (Andrew Ng, DeepLearning.AI, Coursera) — the industry-standard starting point; 2022 version uses Python/NumPy.
**Use alongside it:** StatQuest with Josh Starmer (YouTube, free) — slows down on the algorithms Ng rushes (XGBoost, random forests, ROC curves).

**Primary book:** *Hands-On Machine Learning with Scikit-Learn, Keras, and TensorFlow* (Aurélien Géron) — practical, code-heavy, run it in parallel with Ng's course.
**Reach for when Géron feels thin on "why":** *An Introduction to Statistical Learning* (free, ISLR.org, now has Python labs).

**Optional/advanced:** CS229 Machine Learning (Stanford, Andrew Ng) — [full playlist](https://www.youtube.com/playlist?list=PLoROMvodv4rMiGQp3WXShtMGgzqpfVfbU). *Pattern Recognition and Machine Learning* (Bishop) if going deep on theory. *The Hundred-Page Machine Learning Book* as a dense reference.

## Phase 3 — Deep Learning & Transformers

**Primary course:** Practical Deep Learning for Coders ([fast.ai](https://course.fast.ai/Lessons/lesson1.html), free) — top-down, code-first, matches an engineering background.
**Do not skip:** Andrej Karpathy — *Neural Networks: Zero to Hero* ([playlist](https://www.youtube.com/playlist?list=PLAqhIrjkxbuWI23v9cThsA9GvCAUhRvKZ)) — builds backprop, a language model, and a GPT from scratch, live, in code.
**Read before Karpathy's GPT video:** [The Illustrated Transformer](http://jalammar.github.io/illustrated-transformer/) (Jay Alammar) — best conceptual primer on attention anywhere.
**Supplementary math rigor:** Deep Learning Specialization (Andrew Ng, DeepLearning.AI).

**Primary books:**
- *Deep Learning* (Goodfellow, Bengio, Courville) — the field's reference text. Read Part 1 ("Applied Math and ML Basics") as a bridge from Phase 1, treat the rest as reference.
- *Dive into Deep Learning* (free, [d2l.ai](https://d2l.ai)) — code-first, runnable notebooks, strong transformers chapter.

**Paper (read after Illustrated Transformer + Karpathy):** "Attention Is All You Need."

**Optional detours (only if a project needs them, not FOMO):**
- Computer vision: CS231n (Stanford) — [playlist](https://youtube.com/playlist?list=PLoROMvodv4rOmsNzYBMe0gJY2XS8AQg16); book *Deep Learning for Vision Systems*
- NLP: CS224N — [playlist](https://youtube.com/playlist?list=PLoROMvodv4rOaMFbaqxPDoLWjDaRAdP9D); CS224U NLU — [playlist](https://youtube.com/playlist?list=PLoROMvodv4rPt5D0zs3YhbWSZA8Q_DyiJ); book *Speech and Language Processing*
- Deep generative models: CS236 — [playlist](https://youtube.com/playlist?list=PLoROMvodv4rPOWA-omMM6STXaWW4FvJT8)
- Reinforcement learning: CS234 — [playlist](https://youtube.com/playlist?list=PLoROMvodv4rN4wG6Nk6sNpTEbuOSosZdX); RL Course by David Silver — [playlist](https://www.youtube.com/playlist?list=PLzuuYNsE1EZAXYR4FJ75jcJseBmo4KQ9-)

## Phase 4 — LLMs & Applied AI Engineering

**Primary courses:**
- DeepLearning.AI short courses — "LangChain for LLM Application Development," "Building and Evaluating Advanced RAG," "Finetuning Large Language Models" (short, built with OpenAI/LangChain, stay current)
- [Hugging Face LLM / NLP Course](https://huggingface.co/learn/llm-course) (free) — industry-standard for tokenization, fine-tuning, Transformers library
- Full Stack LLM Bootcamp (free lectures) — the deployment/monitoring/eval gap the above skip

**Primary book:** *Natural Language Processing with Transformers* (Tunstall, von Werra, Wolf — written by Hugging Face engineers), paired directly with the HF course.
**Production-systems book:** *Designing Machine Learning Systems* (Chip Huyen) — data pipelines, evaluation, deployment, monitoring; directly relevant to the Phase 4 capstone.

**Also strong on the "AI Engineer" framing specifically:**
- *AI Engineering* (Chip Huyen, 2025) — the field's current "bible" for building reliable AI systems in production rather than training from scratch
- *Build a Large Language Model (From Scratch)* (Sebastian Raschka) — understand an LLM at the code level
- *The LLM Engineering Handbook* (Paul Iusztin & Maxime Labonne) — practical RAG/fine-tuning/eval how-to
- *Hands-On Large Language Models* (Jay Alammar) — vocabulary and mental models for attention/transformers

**Reference docs:** [OpenAI Platform Docs](https://platform.openai.com/docs), [OpenAI Cookbook](https://cookbook.openai.com/), [LangGraph Docs](https://langchain-ai.github.io/langgraph/), [LlamaIndex Docs](https://docs.llamaindex.ai/), [Pinecone Learn](https://www.pinecone.io/learn/)

**Eval tools to know:** RAGAS, Arize Phoenix, [OpenAI Evals](https://github.com/openai/evals), [Braintrust](https://www.braintrust.dev/)

**Vector DB / fine-tuning ecosystem:** pgvector, Chroma, Weaviate; [unsloth AI docs](https://unsloth.ai/docs) for efficient fine-tuning

## Phase 5 — Agent Engineering & Production

**Docs:** [LangGraph](https://langchain-ai.github.io/langgraph/), [LangSmith](https://docs.smith.langchain.com/), [CrewAI](https://docs.crewai.com/)
**Blogs/communities:** [LangChain Blog](https://blog.langchain.dev/), [Latent Space](https://www.latent.space/)
**Reference repos:** [AI Agents From Scratch](https://github.com/pguso/ai-agents-from-scratch), [AI Engineering from Scratch](https://aiengineeringfromscratch.com/), [Harness Engineering](https://walkinglabs.github.io/learn-harness-engineering/en/lectures/lecture-01-why-capable-agents-still-fail/)
**MLOps book:** *Designing Machine Learning Systems* (Chip Huyen, same as Phase 4) — tools: MLflow, Weights & Biases, Made With ML course

## Papers worth reading, in order (ongoing, across Phase 3-5)

1. Attention Is All You Need
2. BERT: Pre-training of Deep Bidirectional Transformers
3. Language Models are Few-Shot Learners (GPT-3)
4. LoRA: Low-Rank Adaptation of Large Language Models

## The "Core Six" if everything else gets cut

| Area | Resource |
|---|---|
| Mathematics | *Mathematics for Machine Learning* (Deisenroth et al.) |
| Classical ML | *Hands-On Machine Learning* (Géron) |
| Deep Learning | *Dive into Deep Learning* (d2l.ai) |
| LLMs | *Build a Large Language Model (From Scratch)* (Raschka) |
| MLOps | *Designing Machine Learning Systems* (Huyen) |
| Transformers | *Attention Is All You Need* (paper) |

## General link dump (channels, threads, trackers — not phase-specific)

- [AI Engineer roadmap.sh](https://roadmap.sh/ai-engineer)
- [AI-Study-Group](https://github.com/ArturoNereu/AI-Study-Group)
- [ML Research by Teekay](https://github.com/imteekay/machine-learning-research)
- [The Anatomy of an LLM](https://www.royvanrijn.com/anatomy-of-an-llm/#intro)
- [ML Bible (Arjun Virk)](https://www.arjunvirk.com/writing/ml-guide)
- [I Tried 20+ LLM Courses on Udemy — Top 5 for 2026](https://medium.com/javarevisited/i-tried-20-llm-courses-on-udemy-here-are-my-top-5-recommendations-for-2026-b465dae710e3)
- [I Tried 20+ LangChain Courses on Udemy — Top 5 for 2026](https://medium.com/javarevisited/i-tried-20-langchain-courses-on-udemy-here-are-my-top-5-recommendations-for-2026-fde288d7c831)
- [Free Nvidia Courses](https://www.nvidia.com/en-us/training/find-training/?Free+Courses=Free)
- Book repos: [ML Books G Drive](https://drive.google.com/drive/folders/1jIJMyBOeWiVxLCUUtLvEFEFCnWxbh6cs), [AI ML books (GitHub)](https://github.com/AniruddhaChattopadhyay/Books), [ML Notes GitHub](https://github.com/TruongDat05/machine-learning-notes-and-code)
- [How to Learn ML in 2026 (feat. Vicki Boykis, ML Engineer)](https://www.youtube.com/watch?v=vSz-VWb_0tY) — YouTube; general "how to learn ML" video

### Reddit

- [Need advice on how to approach "AI Engineering" by Chip Huyen (non-ML background)](https://www.reddit.com/r/learnmachinelearning/comments/1ltq4hy/need_advice_on_how_to_approach_ai_engineering_by/)
- [6 Months of ML Engineering: the 20% of theory that handles 80% of production code](https://www.reddit.com/r/learnmachinelearning/comments/1tldmd7/6_months_of_ml_engineering_the_20_of_theory_that/)
- ML roadmap video via Reddit thread: [ML roadmap](https://www.youtube.com/watch?v=SU4ryn99huA), [Core ML algorithms playlist](https://www.youtube.com/watch?v=yuaz5RSnWjE&list=PL49M3zg4eCviDbR_LvqnZm_IgNzB_fw29), [ML/AI resume projects](https://www.youtube.com/watch?v=xDQL3vWwcp0&list=PL49M3zg4eCviRD4-hTjS5aUZs3PzAFYkJ), [Fine-tuning Llama walkthrough](https://youtu.be/dn2anUU0d0U)

### X / Twitter threads worth keeping

- [Sam Altman's Advice](https://x.com/benln/status/1953446220992520556)
- [n8n complete beginner's guide](https://x.com/rileybrown_ai/status/1943744716954382610)
- [Zach Wilson's recommended books](https://x.com/EcZachly/status/1884080906186678713)
- [10 AI/ML channels worth following](https://x.com/swapnakpanda/status/1906006240855244818)
- [Getting into AI](https://x.com/iamvakhi/status/1947870475306033331)
- [Mathematics for Computer Science](https://x.com/rohanpaul_ai/status/1841886747162247513)
- [Senior ML engineer advice](https://x.com/ajeetunc/status/1814861052770984263)
- [ML playlist recommendation](https://x.com/Hesamation/status/1917301436951535855)
- [Building your first AI agent](https://x.com/CodeByPoonam/status/1959552597658103957)
- [Goldmine for ML concepts — DataMListic](https://x.com/victor_explore/status/1959631838613499944)
