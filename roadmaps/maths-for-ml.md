# Maths for ML Roadmap

> Distilled from several "math for ML" video breakdowns. The point of this phase
> is **intuition**, not proofs — enough to debug training, interpret models, and
> tune hyperparameters deliberately instead of guessing.
>
> Math learning platforms (Khan Academy, Paul's Notes, MIT OCW, Brilliant, etc.)
> are collected under **Math resources** in [`../resources.md`](../resources.md).

## Guiding principles

- **Start coding before mastering math.** You don't need perfect math before you begin — build ML projects and fill gaps as you hit them.
- **Build visual intuition first.** Get a visual/intuitive grasp (3Blue1Brown) before dense textbooks or grinding problems.
- **Math is about intuition, not proofs.** Focus on practical tools (matrix operations) and conceptual intuition (how derivatives drive optimization), not memorizing complex integrals or proofs.
- **Statistics is the highest-leverage branch.** A strong grasp of statistics makes you dramatically better at ML — it helps you pick the right algorithm, avoid overfitting, and know when a simple model is enough.
- **Purposeful tuning over guessing.** Knowing the math turns hyperparameter tuning into a strategic process instead of trial-and-error.

## The three pillars

1. **Statistics & Probability** — random variables, distributions, central limit theorem, standard deviation, hypothesis testing, Bayes' theorem. The most practical pillar; used for data analysis and applying ML to datasets.
2. **Linear Algebra** — vectors, matrices, inverse, transpose, dot products, eigenvalues/eigenvectors, SVD. The mechanism used to process and format data; especially important for neural networks.
3. **Calculus** — derivatives, gradients, the chain rule, optimization. The engine of optimization that lets networks learn from error.

Then bridge into **ML-specific math concepts:** loss functions, gradient descent, train/test/validation sets, overfitting/underfitting, and the **bias-variance trade-off** (arguably the single most important concept in all of ML).

## Recommended learning order (topics)

1. Statistics & Probability
2. Linear Algebra
3. Calculus
4. ML-specific concepts (loss functions, gradient descent, splits, over/underfitting)

## Recommended resource order

1. **3Blue1Brown** — _Essence of Linear Algebra_ + _Essence of Calculus_ (YouTube). Start here for visual intuition before any formal coursework. Widely regarded as the best math education content on the internet.
2. **Mathematics for Machine Learning Specialization** (Imperial College London, Coursera). The structured, practical course for linear algebra and multivariable calculus.
3. **Khan Academy** — Statistics & Probability (and Linear Algebra / Calculus). Use this to fill the statistics/probability gap the Coursera specialization doesn't cover. Free, beginner-friendly.
4. **An Introduction to Statistical Learning (ISL)** — read parts of it (or the authors' free YouTube series) to connect the math to real ML techniques.
5. **Mathematics for Machine Learning** (eBook, mml-book.com) — final step; ties everything together by showing exactly how these concepts build ML algorithms from scratch.

## Practical note

Because high-level libraries (PyTorch, scikit-learn, TensorFlow) abstract the math away, it's easy to skip — but lacking intuition makes it much harder to debug training issues, interpret behavior, and fix things when they break. Learn just enough to reason about what's happening under the hood.
