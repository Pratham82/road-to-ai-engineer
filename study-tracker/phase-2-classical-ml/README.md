# Phase 2 — Classical ML

**Duration: 8-10 weeks**

## What you're building here

The ability to look at a dataset, pick an appropriate algorithm, train it, and — more importantly — diagnose *why* it's underperforming. Less about memorizing algorithms, more about building diagnostic instincts: bias-variance, overfitting, what a bad confusion matrix is telling you. Don't jump to deep learning before this — simple algorithms are faster, more interpretable, and the foundation for understanding neural nets later.

## Topics, in order

**1. Supervised learning — regression**
- Linear regression, cost functions, gradient descent applied concretely (Phase 1's calculus pays off immediately here)
- Polynomial regression, feature scaling

**2. Supervised learning — classification**
- Logistic regression
- Decision trees, random forests
- Gradient boosting (XGBoost) — one of the most widely used algorithms in industry, don't skip it for being less "famous" than neural nets

**3. Unsupervised learning**
- K-means clustering
- PCA (dimensionality reduction) — Phase 1's eigenvalues/eigenvectors become concrete here

**4. Model evaluation and diagnostics — the most important sub-topic in this phase**
- Bias-variance tradeoff
- Overfitting/underfitting, regularization (L1/L2)
- Train/validation/test splits, cross-validation
- Precision, recall, F1, ROC-AUC, confusion matrices — and *when* each one matters (why accuracy is misleading on imbalanced data)

## Courses & books

See [Curated Resources → Phase 2](../docs/curated-resources.md#phase-2--classical-ml).

## Project work — don't skip this, this phase is where projects matter most

Pick 2-3 Kaggle datasets and run the **full pipeline** each time, not just `model.fit()`: EDA → feature engineering → try 2-3 algorithms → compare using the right metric for that problem → write up what you learned.

Suggested progression:
1. Titanic (classification, small, forgiving)
2. House Prices (regression, needs real feature engineering)
3. A class-imbalance dataset, e.g. fraud detection — forces you to actually understand precision/recall tradeoffs instead of just accuracy

## Checkpoint before moving to Phase 3

See [CHECKPOINT.md](CHECKPOINT.md).

**Fork point worth naming:** everything in this phase transfers directly if you end up on an ML Engineer path instead of AI Engineer — it's the one phase both paths share completely. Phase 3 (deep learning) is where the paths start requiring different depth.
