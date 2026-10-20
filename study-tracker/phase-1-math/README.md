# Phase 1 — Math Foundations

**Duration: 5-7 weeks**

## What you're building here

Enough math intuition to understand *why* an algorithm works, not derive it from a blank page. Enough Python/NumPy/Pandas fluency that data manipulation is never the bottleneck once you get to modeling. You don't need a math PhD — you need working intuition, built visually first, then formalized.

## Learning order (don't skip the order)

The two independent "how to learn this" sources both converge on the same order — intuition before formalism, and this specific topic sequence:

1. **Statistics & Probability first** — this is the highest-leverage branch. It's what stops you from picking the wrong algorithm, misreading results, or shipping a model that doesn't generalize. Distributions, mean/variance/std dev, Bayes' theorem (conceptual), central limit theorem, hypothesis testing.
2. **Linear Algebra** — vectors (a data point, a direction, a weight), matrix multiplication (the core op every NN layer does), dot products, norms, eigenvalues/eigenvectors (conceptual — needed for PCA in Phase 2, don't skip even though it feels abstract now).
3. **Calculus** — derivatives (slope, rate of change), partial derivatives, gradients, chain rule. Internalize the chain rule properly: backpropagation in Phase 3 *is* the chain rule applied repeatedly. Skip trying to memorize integration rules — you need derivatives and optimization intuition, not a calc exam.
4. **ML-specific math concepts** — loss functions, gradient descent, train/test/validation splits, overfitting/underfitting, bias-variance tradeoff (the single most important concept in all of ML).

## The core mental model (worth internalizing early)

Don't memorize formulas — ask what each one is *trying to accomplish* and translate it to natural language. Linear regression's loss function is just the formal way of telling a computer "find the line with the shortest vertical distance to these points." Math intuition (especially statistics) is what makes hyperparameter tuning strategic instead of guessing, and what tells you when a simple model is already good enough.

## Courses & books

See [Curated Resources → Phase 1](../docs/curated-resources.md#phase-1--math-foundations) for the full list, in recommended order (3Blue1Brown → Khan Academy / Imperial College Coursera → ISL → MML book).

## Checkpoint before moving to Phase 2

See [CHECKPOINT.md](CHECKPOINT.md). If any item feels shaky, spend an extra week here rather than pushing into Phase 2 with gaps — Phase 2 leans on this constantly.

**Checkpoint project:** full EDA on a real dataset in Pandas.
