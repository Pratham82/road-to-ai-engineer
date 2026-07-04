# Phase 1: Math + Python Foundations

Here's the full breakdown of Phase 1 — the foundation everything else in the roadmap sits on.

## What you're building here

Enough math intuition to understand _why_ an algorithm works, not derive it from a blank page. Enough Python/NumPy/Pandas fluency that data manipulation is never the bottleneck when you get to modeling.

## Topics, in order

**1. Linear algebra**

- Vectors and what they represent (a data point, a direction, a weight)
- Matrices and matrix multiplication — this is the core operation every neural net layer does
- Dot products, norms
- Eigenvalues/eigenvectors (conceptual — you need this for PCA in Phase 2, don't skip it even though it feels abstract now)

**2. Calculus**

- Derivatives and what they mean geometrically (slope, rate of change)
- Partial derivatives, gradients
- Chain rule — internalize this properly, since backpropagation in Phase 3 _is_ the chain rule applied repeatedly

**3. Probability & statistics**

- Distributions (normal, binomial — just enough to reason about data)
- Mean, variance, standard deviation
- Bayes' theorem (conceptual understanding, not exam-level derivation)

**4. Python tooling**

- NumPy: arrays, broadcasting, vectorized operations (this replaces loops — important habit to build early)
- Pandas: dataframes, groupby, merging, cleaning

## Courses

- **3Blue1Brown** — "Essence of Linear Algebra" + "Essence of Calculus" (YouTube, free) — watch these _first_, before anything formal. Pure visual intuition, no exercises, ~5-6 hours total combined.
- **Mathematics for Machine Learning Specialization** (Imperial College London, Coursera) — the structured, industry-standard course that turns the 3Blue1Brown intuition into actual working knowledge, with ML-specific framing throughout.
- **Kaggle micro-courses** — "Pandas" and "Intro to Machine Learning" (free, a few hours each) — practical, code-first, good for building NumPy/Pandas muscle memory without a heavy course commitment.

## Book

- **Mathematics for Machine Learning** by Deisenroth, Faisal, Ong — widely considered the modern gold standard for beginners and intermediates, explicitly designed to bridge traditional math textbooks and practical programming, with the first half covering pure math concepts and the second half showing exactly how those equations power algorithms like SVMs and PCA. Free PDF at mml-book.com — use it as a companion to the Imperial College course rather than reading it cover-to-cover separately; when a course concept feels thin, that's when you open the matching chapter.

## Suggested weekly rhythm (at 8-10 hrs/week)

- 2-3 hrs: Imperial College course modules
- 2-3 hrs: Kaggle micro-courses / NumPy-Pandas practice
- 2-3 hrs: 3Blue1Brown (early weeks only, tapers off)
- 1-2 hrs: book reference reading, as needed

## Checkpoint before moving to Phase 2

You should be able to:

- Explain gradient descent using an actual derivative, not just "it goes downhill"
- Do a full exploratory data analysis (cleaning, aggregation, basic visualization) on a real dataset in Pandas without looking up basic syntax
- Multiply two matrices by hand for a small example and explain what the operation represents

If any of these feel shaky, it's worth an extra week here rather than pushing into Phase 2 with gaps — the classical ML phase leans on this constantly.
