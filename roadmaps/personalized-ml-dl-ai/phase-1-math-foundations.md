# Phase 1: Math Foundations

Here's the full breakdown of Phase 1 — the foundation everything else in the roadmap sits on. (Python and NumPy/Pandas tooling now live in [Phase 0](phase-0-python-for-ai.md).)

**Duration: 5-7 weeks**

## What you're building here

Enough math intuition to understand _why_ an algorithm works, not derive it from a blank page. Enough Python/NumPy/Pandas fluency that data manipulation is never the bottleneck once you get to modeling. You don't need a math PhD — you need working intuition, built visually first, then formalized.

## Learning order (don't skip the order)

Intuition before formalism, and this specific topic sequence:

**1. Statistics & probability first** — the highest-leverage branch. It's what stops you from picking the wrong algorithm, misreading results, or shipping a model that doesn't generalize.

- Distributions (normal, binomial — just enough to reason about data)
- Mean, variance, standard deviation
- Bayes' theorem (conceptual understanding, not exam-level derivation)
- Central limit theorem, hypothesis testing

**2. Linear algebra**

- Vectors and what they represent (a data point, a direction, a weight)
- Matrices and matrix multiplication — this is the core operation every neural net layer does
- Dot products, norms
- Eigenvalues/eigenvectors (conceptual — you need this for PCA in Phase 2, don't skip it even though it feels abstract now)

**3. Calculus**

- Derivatives and what they mean geometrically (slope, rate of change)
- Partial derivatives, gradients
- Chain rule — internalize this properly, since backpropagation in Phase 3 _is_ the chain rule applied repeatedly
- Skip memorizing integration rules — you need derivatives and optimization intuition, not a calc exam

**4. ML-specific math concepts**

- Loss functions, gradient descent
- Train/test/validation splits
- Overfitting/underfitting
- Bias-variance tradeoff — the single most important concept in all of ML

## The core mental model (worth internalizing early)

Don't memorize formulas — ask what each one is _trying to accomplish_ and translate it to natural language. Linear regression's loss function is just the formal way of telling a computer "find the line with the shortest vertical distance to these points."

## Courses

Primary path, in order:

1. **3Blue1Brown** — "Essence of Linear Algebra" + "Essence of Calculus" (YouTube, free) — watch these _first_, before anything formal. Pure visual intuition, no exercises, ~5-6 hours total combined.
2. **Khan Academy** — Statistics & Probability (free, ~50 hrs) → Linear Algebra (1-2 wks) → Calculus (1-2 wks)
3. **Mathematics for Machine Learning Specialization** (Imperial College London, Coursera) — the structured, industry-standard course that turns the 3Blue1Brown intuition into actual working knowledge, with ML-specific framing throughout.
4. **An Introduction to Statistical Learning (ISLR)** — free at statlearning.com, or the authors' free YouTube series — connects the math to real ML techniques.

Also in the original plan: **Kaggle micro-courses** — "Pandas" and "Intro to Machine Learning" (free, a few hours each) — good for building NumPy/Pandas muscle memory.

## Book

- **Mathematics for Machine Learning** by Deisenroth, Faisal, Ong — widely considered the modern gold standard for beginners and intermediates, explicitly designed to bridge traditional math textbooks and practical programming, with the first half covering pure math concepts and the second half showing exactly how those equations power algorithms like SVMs and PCA. Free PDF at mml-book.com — use it as a companion to the Imperial College course rather than reading it cover-to-cover separately; when a course concept feels thin, that's when you open the matching chapter.

## Suggested weekly rhythm (at 8-10 hrs/week)

- 2-3 hrs: Imperial College course modules
- 2-3 hrs: Khan Academy / Kaggle micro-courses / NumPy-Pandas practice
- 2-3 hrs: 3Blue1Brown (early weeks only, tapers off)
- 1-2 hrs: book reference reading, as needed

## Checkpoint before moving to Phase 2

You should be able to:

- Explain gradient descent using an actual derivative, not just "it goes downhill"
- Do a full exploratory data analysis (cleaning, aggregation, basic visualization) on a real dataset in Pandas without looking up basic syntax
- Multiply two matrices by hand for a small example and explain what the operation represents
- Explain the bias-variance tradeoff in your own words

If any of these feel shaky, it's worth an extra week here rather than pushing into Phase 2 with gaps — the classical ML phase leans on this constantly.

**Checkpoint project:** full EDA on a real dataset in Pandas.
