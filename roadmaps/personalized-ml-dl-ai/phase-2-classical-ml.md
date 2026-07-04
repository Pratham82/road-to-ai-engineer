# Phase 2: Classical Machine Learning

Here's the full breakdown of Phase 2 — this is where math starts turning into actual working models.

## What you're building here

The ability to look at a dataset, pick an appropriate algorithm, train it, and — more importantly — diagnose _why_ it's underperforming. This phase is less about memorizing algorithms and more about building the diagnostic instincts (bias-variance, overfitting, what a bad confusion matrix is telling you).

## Topics, in order

**1. Supervised learning — regression**

- Linear regression, cost functions, gradient descent applied concretely (this is where Phase 1's calculus pays off immediately)
- Polynomial regression, feature scaling

**2. Supervised learning — classification**

- Logistic regression
- Decision trees, random forests
- Gradient boosting (XGBoost) — this is genuinely one of the most widely used algorithms in industry, don't skip it even though it's less "famous" than neural nets

**3. Unsupervised learning**

- K-means clustering
- PCA (dimensionality reduction) — this is where Phase 1's eigenvalues/eigenvectors become concrete

**4. Model evaluation and diagnostics — the most important sub-topic in this phase**

- Bias-variance tradeoff
- Overfitting/underfitting, regularization (L1/L2)
- Train/validation/test splits, cross-validation
- Evaluation metrics: precision, recall, F1, ROC-AUC, confusion matrices — and _when_ each one matters (e.g. why accuracy is misleading on imbalanced data)

## Courses

- **Machine Learning Specialization** (Andrew Ng, DeepLearning.AI, Coursera) — the definitive starting point industry-wide, three courses covering supervised ML, advanced algorithms, and unsupervised/recommenders/reinforcement learning basics. Updated 2022 version uses Python/NumPy, not the old Octave version.
- **StatQuest with Josh Starmer** (YouTube, free) — use this _alongside_ Ng's course, not instead of it. Ng moves through algorithms efficiently; StatQuest slows down on the specific ones that feel rushed (XGBoost, random forests, ROC curves especially).

## Book

- **Hands-On Machine Learning with Scikit-Learn, Keras, and TensorFlow** by Aurélien Géron — a practical guide to building ML systems in Python, not a theory book, covering the full pipeline: data cleaning, feature engineering, model training, evaluation, and deployment basics. This is the one to actually work through in parallel with Ng's course — it's code-heavy and matches how you already like to learn (given your engineering background).
- **An Introduction to Statistical Learning (ISLR)** by James, Witten, Hastie, Tibshirani — still relevant for foundations like the bias-variance trade-off, cross-validation, regularization, and model selection, though it doesn't cover deep learning or anything post-2015. Free PDF at ISLR.org, with Python labs added recently. Reach for this once Géron's explanations start feeling thin on the "why" — it's the bridge between practical ML and the more mathematical treatment.

## Suggested weekly rhythm (at 8-10 hrs/week)

- 3-4 hrs: Andrew Ng's course modules + assignments
- 2-3 hrs: Géron's book, working through code examples in parallel with whatever Ng covers that week
- 1-2 hrs: StatQuest videos for whichever algorithm needs more intuition that week
- 1-2 hrs: Kaggle project work

## Project work (don't skip this — this phase is where projects matter most)

Pick 2-3 Kaggle datasets and run the **full pipeline** each time, not just model.fit():

- EDA → feature engineering → try 2-3 different algorithms → compare using the right evaluation metric for that problem → write up what you learned

Suggested progression: start with Titanic (classification, small, forgiving), then House Prices (regression, needs real feature engineering), then something with class imbalance (fraud detection datasets are common on Kaggle) — that third one forces you to actually understand precision/recall tradeoffs rather than just accuracy.

## Checkpoint before moving to Phase 3

You should be able to:

- Look at a confusion matrix and explain what's actually wrong with a model, not just report its accuracy
- Explain why a model is overfitting and pick an appropriate fix (more data, regularization, simpler model, etc.)
- Justify why you chose a particular algorithm for a particular dataset, not just "because the tutorial used it"

This phase is also a genuine fork point worth naming: everything here transfers directly if you end up going ML Engineer route instead of AI Engineer — it's the one phase both paths share completely. Deep learning (Phase 3) is where the paths would start requiring different depth.
