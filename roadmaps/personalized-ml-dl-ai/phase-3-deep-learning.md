# Phase 3: Deep Learning

Here's the full breakdown of Phase 3 — the most important phase in the entire roadmap, and the one that actually separates "genuine DL foundations" from "wrapper-level AI engineer."

## What you're building here

Understanding of how neural networks actually learn (not just how to call `model.fit()` in PyTorch), and deep, working intuition for transformers specifically — since that architecture underlies everything you'll do in Phase 4. This is also the phase where math from Phase 1 stops being abstract and becomes the actual mechanism.

## Topics, in order

**1. Neural network fundamentals**

- Perceptrons → multi-layer networks
- Forward propagation
- **Backpropagation** — understand it conceptually, and be able to derive it by hand for a simple network at least once. This is the single biggest gap between people who "use" DL and people who understand it.
- Activation functions: sigmoid, tanh, ReLU — and why ReLU won over the older ones
- Loss functions: MSE, cross-entropy
- Optimizers: SGD, momentum, Adam — and why Adam became the default
- Weight initialization, vanishing/exploding gradients

**2. PyTorch fluency**

- Tensors, autograd, `nn.Module`, DataLoaders
- Training loops, learning rate scheduling
- Debugging basics: shape mismatches, NaN losses, gradient checking

**3. CNNs (compressed for you)**

- Convolution, pooling, feature maps — conceptual understanding is enough
- Skip connections (ResNet) — worth knowing since this concept reappears in transformers
- Transfer learning — you'll use this idea (fine-tuning pretrained models) constantly in Phase 4, just applied to language models instead of images

_Given your target is AI Engineering rather than computer vision, don't over-invest here — understand it, don't master it._

**4. Transformers — the centerpiece of this entire roadmap**

- Self-attention: what a query, key, and value actually are, and what the attention computation is doing geometrically
- Multi-head attention, positional encoding
- Encoder-only (BERT-style) vs decoder-only (GPT-style) vs encoder-decoder (T5-style) — and _why_ decoder-only won for the LLM era
- Tokenization basics (deeper dive comes in Phase 4)

## Courses

- **Practical Deep Learning for Coders** (fast.ai, free) — top-down, code-first. Given your engineering background, this should be your primary course — you build working models first, then understand the theory underneath, rather than the reverse.
- **Deep Learning Specialization** (Andrew Ng, DeepLearning.AI) — use as a supplementary reference for the math rigor fast.ai moves past quickly.
- **Neural Networks: Zero to Hero** (Andrej Karpathy, YouTube, free) — do not skip this one. Karpathy builds backpropagation, a language model, and eventually a GPT from scratch, live, in code. This is widely regarded as the best from-scratch resource that exists for engineers who learn by reading code.
- **The Illustrated Transformer** (Jay Alammar, blog, free) — read this before Karpathy's GPT video. Best conceptual primer on attention available anywhere.
- **CS224n: NLP with Deep Learning** (Stanford, free lectures) — optional, for academic-level depth specifically on transformers, if you want the university treatment.

## Reading

- **"Attention Is All You Need"** (original paper) — read this _after_ Illustrated Transformer + Karpathy's video. At that point it'll actually be legible rather than dense jargon.

## Books

- **Deep Learning** by Goodfellow, Bengio, Courville — often called the "Bible of Deep Learning," written by pioneers of the field, contextualizing the math within deep learning and showing exactly why each formula matters, though it reads more like a reference manual than a tutorial. Part 1 specifically ("Applied Math and Machine Learning Basics") is considered one of the best mathematical crash courses available anywhere — read that part as a bridge from Phase 1's math, then treat the rest as a reference to dip into rather than read cover-to-cover.
- **Dive into Deep Learning (d2l.ai)** — free, code-first, interactive notebooks alongside every concept. Pairs naturally with fast.ai's style, and has a genuinely strong transformers chapter.

## Suggested weekly rhythm (at 8-10 hrs/week)

- 3-4 hrs: fast.ai lessons + notebooks
- 2-3 hrs: Karpathy's Zero to Hero series (front-load this early in the phase, it sets up everything else)
- 1-2 hrs: Illustrated Transformer + CS224n lectures (once you hit the transformer section)
- 1-2 hrs: Goodfellow/d2l.ai as reference reading when a concept needs more depth

## Projects (in order)

1. **Backprop from scratch in raw NumPy** (MNIST digit classification) — the rite of passage. Forces you to actually implement the chain rule once instead of trusting a framework.
2. **Rebuild the same project in PyTorch** — compare against your NumPy version, appreciate what the framework handles for you.
3. **Karpathy's GPT-from-scratch**, then extend it yourself — train on a different dataset, tweak the architecture, see what breaks and why.

## Checkpoint before moving to Phase 4

You should be able to:

- Derive backpropagation for a simple 2-layer network by hand
- Explain what self-attention is computing, geometrically — not just "tokens look at each other"
- Explain why decoder-only architectures won for the LLM era
- Debug a training loop that's producing NaN losses or not converging

This is also the phase where I'd flag: it's fine to take longer than the 12-16 week estimate here. Given you have no rush and this phase determines whether you actually have "deep foundations" or just another certificate, protecting the transformer section specifically is worth extra time if it needs it.
