# Community Study Approaches

> Distilled, attributed summaries of how experienced people actually studied ML —
> useful for *how to learn*, not just *what to learn*. Treat these as mental
> models to layer on top of the structured roadmaps.

---

## 0xhadyy — Learning-in-Public Phased Path

Source: [youtube.com/@0xhadyy](https://www.youtube.com/@0xhadyy). A creator documenting his own ML journey week-by-week and month-by-month.

> **Note:** In the original notes, several of 0xhadyy's per-video links were Google-search redirect URLs rather than clean YouTube links. Verify individual videos directly on his channel.

**Phase 1 — Math Foundations & First Iterations (Months 1–3):** Clear the mathematical friction to understand *why* algorithms work before writing complex code. Videos track weekly progress ("Week 1/2/3 of Studying ML", "1/2/3 Months of ML", including the motivation/burnout wall around weeks 6–7).

- Books: *Mathematics for Machine Learning* (Calculus + Linear Algebra), *Probability and Statistics for Machine Learning* (real examples + full solution keys), *An Introduction to Statistical Learning (with Applications in Python)* as the primary ML textbook (the "perfect mix" of theory + applied programming).
- Code: NumPy, Matplotlib, Pandas, Jupyter Notebooks on the textbook's official datasets.
- Note-taking stack: Pen & paper (first pass) → **Obsidian** (second pass after a week) → rendered with **LaTeX** for clean formulas.

**Phase 2 — Algorithmic Mechanics From Scratch (concurrent):** Strip out the abstractions and code the math directly instead of treating scikit-learn as a black box. Topics implemented from scratch: linear regression, gradient descent, ridge regression, logistic regression, PCA via SVD. Dual-tracks *ISLP* (concepts) and *Hands-On ML* (applied reference).

**Phase 3 — Workflow Optimization & Scaling (Months 4–6):** Refine how you consume material — note organization, resource auditing, progress evaluation. Re-architect Obsidian with linked graph connections; publish notebooks/figures/datasets to **GitHub** for external accountability. Includes an honest "5 Months — 50 days wasted" retro on lost momentum and realigning a plan.

**Phase 4 — Applied Deep Learning & Paper Implementations (Year 1+):** Shift into modern architectures — NLP, attention, academic literacy.

- Books: *Dive into Deep Learning (D2L)* (main), *Deep Learning* (Goodfellow, reference supplement).
- Playlists/sites: Karpathy's **Neural Networks: Zero to Hero**, **Hugging Face Learn**.
- Toolstack: PyTorch (over TensorFlow), FastAPI, Hugging Face Transformers, ONNX.
- Strategy: read 3–4 foundational papers to learn academic language, while strictly filtering out side-tracks (diffusion, RL, graph nets) to stay focused.

---

## Egor Howell — "Stop Taking Random AI Courses, Read These Books Instead"

A depth-wise, book-led roadmap for the modern **AI Engineer** era.

**Key ideas:**

- **The AI Engineer role** is closer to backend software engineering than traditional ML — you build infrastructure and products around existing foundational models rather than training new ones. Backend languages (Rust, Go, Java) are increasingly relevant alongside Python.
- **Math is non-negotiable for top-tier work** — Statistics, Linear Algebra, Calculus — even though APIs abstract much of it.
- **AI is broader than Generative AI.** Master traditional ML before deep learning; GenAI is a recent subset.
- **PyTorch > TensorFlow** — the industry/research standard.
- **Depth-wise learning (Karpathy-style):** build a concrete project, learn only what that project requires on demand, summarize learnings in your own words. Prevents tutorial hell and burnout.

**Ordered roadmap:**

1. **Programming Fundamentals** — Python (FreeCodeCamp / Python for Everybody).
2. **CS Basics** — Data Structures, Algorithms, System Design (NeetCode / Harvard CS50).
3. **Core Mathematics** — *Practical Statistics for Data Science*, then *Mathematics for Machine Learning* (book/course) for linear algebra + calculus.
4. **Traditional ML** — *Hands-On Machine Learning*, then Andrew Ng's ML Specialization. (*The Hundred-Page Machine Learning Book* as a fast reference.)
5. **Deep Learning** — Learn PyTorch, Andrew Ng's Deep Learning Specialization, Karpathy's "Intro to LLMs" + "Zero to Hero".
6. **Transformers & LLMs** — *Hands-On Large Language Models* by Jay Alammar.
7. **AI Engineering & Deployment (MLOps)** — *Practical MLOps* and Chip Huyen's *AI Engineering*.

---

## "Learn Machine Learning Like a GENIUS (and Not Waste Time)"

A practical, no-nonsense roadmap emphasizing foundations and real projects over tutorial hell.

**Principles:**

- **Master "learning how to learn."** Frameworks and papers change fast — adaptability beats memorization.
- **Pareto (80/20):** 80% of results come from 20% of effort — focus on foundations like data prep and basic algorithms.
- **Don't jump to deep learning.** Start with linear/logistic regression — faster, interpretable, and the foundation for understanding neural nets.
- **Math is intuition, not proofs.** Focus on practical tools and conceptual intuition.
- **The "Implement 3 Ways" strategy:** implement a new algorithm (1) from scratch in basic Python, (2) with a library like scikit-learn on a toy dataset, (3) on a real, messy dataset you prepared.
- **Avoid tutorial hell.** Limit to 1–2 tutorials per topic, then build your own project. Trick: take a tutorial, swap the dataset, break the code, force yourself to fix it.
- **Data prep is everything** — 60–80% of the job is EDA and data preparation.
- **Collaborate to learn 10x faster** — coding buddies on Discord / Reddit / Kaggle; get advanced devs to critique your code.

**The roadmap (in order):**

1. Python & Jupyter Notebooks (variables, loops, dicts, functions).
2. Pandas tutorial (merging, reshaping, cleaning).
3. **First data analysis project** — clean a real dataset, plot correlations, turn it into a presentation (before any ML).
4. Khan Academy — Statistics & Probability (~50 hrs, the most important math branch).
5. Khan Academy — Linear Algebra (1–2 weeks).
6. Khan Academy — Calculus (1–2 weeks: derivatives, chain rule, optimization).
7. *An Introduction to Statistical Learning* (book or the authors' free YouTube series) — theory behind simple ML algorithms.
8. Scikit-Learn tutorial — implement what you learned via "Implement 3 Ways".
9. **First ML project on Kaggle** — start simple, scale complexity, evaluate against a test set.
10. Advanced topics (deep learning, CNNs, RNNs, Transformers) — **learn by need**, only when a project actually requires them. No FOMO.
