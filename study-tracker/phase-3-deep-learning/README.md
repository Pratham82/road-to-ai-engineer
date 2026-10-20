# Phase 3 — Deep Learning & Transformers

**Duration: 12-16 weeks** — the most important phase in the roadmap; the one that separates "genuine DL foundations" from "wrapper-level AI engineer." Fine to run over estimate, especially on the transformer section.

## What you're building here

Understanding of how neural networks actually learn (not just how to call `model.fit()` in PyTorch), and deep, working intuition for transformers specifically — that architecture underlies everything in Phase 4. This is also where Phase 1's math stops being abstract and becomes the actual mechanism.

## Topics, in order

**1. Neural network fundamentals**
- Perceptrons → multi-layer networks, forward propagation
- **Backpropagation** — understand conceptually, and be able to derive it by hand for a simple network at least once. This is the single biggest gap between people who "use" DL and people who understand it.
- Activation functions: sigmoid, tanh, ReLU (and why ReLU won)
- Loss functions: MSE, cross-entropy
- Optimizers: SGD, momentum, Adam (and why Adam became default)
- Weight initialization, vanishing/exploding gradients

**2. PyTorch fluency** (industry default over TensorFlow — dominates research papers and Hugging Face)
- Tensors, autograd, `nn.Module`, DataLoaders
- Training loops, learning-rate scheduling
- Debugging basics: shape mismatches, NaN losses, gradient checking

**3. CNNs (compressed — not your target domain)**
- Convolution, pooling, feature maps — conceptual understanding is enough
- Skip connections (ResNet) — the concept reappears in transformers
- Transfer learning — you'll use this idea constantly in Phase 4, applied to language models instead of images

**4. Transformers — the centerpiece of this entire roadmap**
- Self-attention: what query/key/value actually are, what the attention computation does geometrically
- Multi-head attention, positional encoding
- Encoder-only (BERT) vs decoder-only (GPT) vs encoder-decoder (T5) — and *why* decoder-only won for the LLM era
- Tokenization basics (deeper dive in Phase 4)

## Courses & books

See [Curated Resources → Phase 3](../docs/curated-resources.md#phase-3--deep-learning--transformers). Primary course: fast.ai (top-down, code-first — matches an engineering background). Do not skip Karpathy's Zero to Hero series.

## Reading

**"Attention Is All You Need"** — read *after* The Illustrated Transformer + Karpathy's GPT video, not before. At that point it's legible instead of dense jargon.

## Projects, in order

1. **Backprop from scratch in raw NumPy** (MNIST digit classification) — the rite of passage, forces you to implement the chain rule once instead of trusting a framework.
2. **Rebuild the same project in PyTorch** — compare against the NumPy version, appreciate what the framework handles for you.
3. **Karpathy's GPT-from-scratch**, then extend it — different dataset, tweak the architecture, see what breaks and why.

## Checkpoint before moving to Phase 4

See [CHECKPOINT.md](CHECKPOINT.md).

> Optional depth beyond this phase (CV-specific or NLP-specific coursework — CS231n, CS224N) is listed in the resources note but is a detour, not the main path, unless a project specifically demands it.
