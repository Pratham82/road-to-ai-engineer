**Not a phase.** A standalone prep folder/module, used alongside the roadmap, not in place of it. Nothing here changes phase order, and it adds no new courses or resources. Each section is a checklist of questions to answer *out loud* in your own words, with a pointer to the phase that teaches it.

## How to use

- Work through a section only after you've finished the matching phase. Don't pre-study interview answers for material you haven't learned yet.
- For each question, aim for a 60-90 second spoken answer: **intuition first, then the mechanism, then a concrete example from something you've built.**
- Priority tags: **[core]** asked almost everywhere, **[likely]** asked often for AI Engineer roles, **[deep]** separates strong candidates, **[gap]** not yet covered in the phase notes (we'll cover it when we reach that phase, or flag it for a later pass).
- Mark a question done only when you can answer it without notes.

---

## 1. Python coding & language
*Taught in: [Phase 0 - Python for AI](../phase-0-python/). Solve each without looking anything up, then state time and space complexity.*

### Language concepts
- [ ] [core] Mutable vs immutable types; why a mutable default argument (`def f(x=[])`) is a bug
- [ ] [core] List vs tuple vs set vs dict: when each, and their lookup/insert complexity
- [ ] [core] List comprehension vs generator expression: memory behavior and when to pick which
- [ ] [core] Iterator vs iterable vs generator; what `yield` does to a function
- [ ] [core] Decorators: write one from scratch (e.g. a timing or retry decorator); why `functools.wraps`
- [ ] [likely] Context managers: `with` statement, `__enter__`/`__exit__`, `contextlib.contextmanager`
- [ ] [likely] Dataclasses vs plain classes vs Pydantic models (ties to FastAPI)
- [ ] [likely] Type hints: what they do and don't enforce at runtime
- [ ] [likely] `*args` / `**kwargs`; shallow vs deep copy
- [ ] [likely] `is` vs `==`
- [ ] [deep] The GIL: what it is, what it does to threads vs processes vs asyncio
- [ ] [deep] Threading vs multiprocessing vs asyncio: which for CPU-bound, which for I/O-bound (LLM API calls)
- [ ] [likely] `async`/`await`: what an event loop is; `asyncio.gather` vs sequential awaits; why a blocking call inside async code is a bug
- [ ] [likely] Virtual environments and dependency management: why they exist, how you set yours up

### NumPy / Pandas
- [ ] [core] Vectorized operation vs loop: what's actually faster and why
- [ ] [core] Broadcasting: explain with a shape example
- [ ] [likely] Pandas: `merge` vs `join` vs `concat`; `groupby` + `agg`; handling missing values
- [ ] [likely] `loc` vs `iloc`; why chained indexing is a problem

### Coding problems
**Problem 1: flatten a nested list**
```
ip = [1, [2, [3, 4]], 5]
op = [1, 2, 3, 4, 5]
```
- [ ] [core] Recursive solution
- [ ] [core] Generator-based solution (ties to Phase 0: generators)
- [ ] [likely] Iterative solution with a stack
- [ ] [likely] What breaks on deeply nested input (recursion limit), and what's the fix

**Problem 2: character frequency**
```
ip = "google"
op = {'g': 2, 'o': 2, 'l': 1, 'e': 1}
```
- [ ] [core] Manual dict loop
- [ ] [core] `collections.Counter`
- [ ] [core] Which one would you write in an interview, and why

**More problems worth being able to solve cold**
- [ ] [core] Two-sum (hash map); check whether two strings are anagrams
- [ ] [core] Top-K most frequent elements (heap vs sort vs Counter.most_common)
- [ ] [likely] LRU cache (`OrderedDict`, or doubly linked list + dict)
- [ ] [likely] Retry-with-exponential-backoff decorator (ties to flaky LLM API calls)
- [ ] [likely] Call 20 URLs concurrently with a limit of 5 in flight (`asyncio.Semaphore`)
- [ ] [likely] Split a text into chunks of N words with M words of overlap (ties to RAG chunking)
- [ ] [likely] Cosine similarity between two vectors in NumPy; then top-K nearest from a matrix of vectors
- [ ] [likely] Numerically stable softmax (why subtract the max)
- [ ] [deep] Implement a tiny in-memory vector search from scratch, no libraries beyond NumPy
- [ ] [deep] Parse a stream of JSON chunks (like an LLM streaming response) into complete objects

*Practice problems like these go in a GitHub folder. One short solution plus complexity note each.*

---

## 2. Math & statistics foundations
*Taught in: [Phase 1 - Math Foundations](../phase-1-math/). Interviewers test intuition, not derivations.*

- [ ] [core] Mean vs median; variance and standard deviation; when mean misleads
- [ ] [core] Normal distribution and what the central limit theorem says in plain words
- [ ] [core] Bayes' theorem with a numeric example (e.g. a test for a rare condition)
- [ ] [likely] Correlation vs causation; why correlation can mislead
- [ ] [likely] p-value: what it means and a common way it's misread
- [ ] [core] Dot product: what it computes and why it measures similarity
- [ ] [core] What matrix multiplication represents in a neural-network layer
- [ ] [likely] Norms (L1 vs L2): what each measures and where they show up (regularization, distance)
- [ ] [likely] Eigenvectors in plain words; what PCA uses them for
- [ ] [core] Derivative and gradient: what each tells you
- [ ] [core] Chain rule and why backprop is just the chain rule repeated
- [ ] [core] Gradient descent using an actual derivative (do one numeric step by hand)
- [ ] [core] Bias-variance tradeoff in your own words
- [ ] [likely] Why we split train / validation / test; what data leakage is

---

## 3. Classical ML
*Taught in: [Phase 2 - Classical ML](../phase-2-classical-ml/).*

- [ ] [core] Supervised vs unsupervised vs reinforcement learning, with one example each
- [ ] [core] Regression vs classification
- [ ] [core] Overfitting vs underfitting: how to detect each from train/validation curves, and fixes
- [ ] [core] L1 vs L2 regularization: what each does to weights
- [ ] [core] Cross-validation: what it is and when to use it
- [ ] [core] Precision, recall, F1, ROC-AUC: define each and say when each matters
- [ ] [core] Why accuracy is misleading on imbalanced data; ways to handle imbalance
- [ ] [likely] Read a confusion matrix and say what's wrong with the model
- [ ] [likely] Logistic regression: why it's classification despite the name
- [ ] [likely] Decision tree vs random forest vs gradient boosting: how each reduces error
- [ ] [likely] Why XGBoost is still heavily used on tabular data
- [ ] [likely] K-means: how it works, how to choose K, where it fails
- [ ] [likely] PCA: what it does and when you'd use it
- [ ] [likely] Feature scaling: which algorithms need it and which don't
- [ ] [deep] Feature engineering decision on a dataset you've worked on (Titanic / House Prices / fraud)
- [ ] [deep] Pick an algorithm for a given problem and justify it, not "because the tutorial used it"

---

## 4. Deep learning
*Taught in: [Phase 3 - Deep Learning & Transformers](../phase-3-deep-learning/).*

- [ ] [core] Neural network from scratch conceptually: neuron, layer, forward pass, loss, backward pass, update
- [ ] [core] Backpropagation: explain in plain words, then derive for a tiny 2-layer network
- [ ] [core] Activation functions: sigmoid, tanh, ReLU; why ReLU won; what dying ReLU is
- [ ] [core] Loss functions: MSE vs cross-entropy and which for what
- [ ] [core] Optimizers: SGD, momentum, Adam; why Adam became the default
- [ ] [core] Learning rate: too high vs too low; what a scheduler does
- [ ] [likely] Vanishing and exploding gradients: cause, symptoms, fixes (init, normalization, clipping, skip connections)
- [ ] [likely] Weight initialization: why not all zeros
- [ ] [likely] Batch size effects; epoch vs iteration vs batch
- [ ] [likely] Dropout, early stopping, weight decay: what each regularizes
- [ ] [likely] Batch norm vs layer norm; why transformers use layer norm
- [ ] [likely] Debug a training loop where the loss is NaN or won't decrease
- [ ] [likely] Skip/residual connections: what problem they solve
- [ ] [likely] Transfer learning: what it is, and how it carries over to language models
- [ ] [likely] CNN: convolution, pooling, feature maps in plain words
- [ ] [deep] Why are GPUs fast for this? (parallel matrix math); memory vs compute bottlenecks
- [ ] [deep] PyTorch: tensors, autograd, `nn.Module`, `.train()` vs `.eval()`, `torch.no_grad()`
- [ ] [deep] Mixed precision (fp16/bf16): why it's used and what the risk is

---

## 5. Transformer
*Taught in: [Phase 3 - Deep Learning & Transformers](../phase-3-deep-learning/) (architecture, attention, RNN/LSTM history) and [Phase 4 - LLMs & Applied AI Engineering](../phase-4-llm-engineering/) (KV cache, inference).*

### Landscape
- [ ] [core] Latest open-source and closed LLMs, with versions (**look this up fresh the week before the interview. It goes stale fast; don't memorize from this note**)
- [ ] [likely] How do you choose between a closed API model and an open-weight model for a project? (cost, privacy, latency, control, quality)

### Before transformers
- [ ] [core] What did we use before transformers? RNN, LSTM
- [ ] [core] Problems with RNN/LSTM: exploding gradients, vanishing gradients
- [ ] [likely] Why RNNs can't be parallelized across the sequence, and why that mattered at scale
- [ ] [likely] What an LSTM's gates fix, and why they didn't fully solve long-range dependence

### Architecture
- [ ] [core] Transformer architecture, end to end (input → embeddings → blocks → output)
- [ ] [core] Self-attention: Q, K, V and what the computation does
- [ ] [core] Why divide by √d_k in scaled dot-product attention
- [ ] [core] Self-attention vs multi-head attention; why multiple heads
- [ ] [core] Positional encoding: why it's needed, and the main kinds (sinusoidal, learned, RoPE)
- [ ] [core] Activation in the last layer: Softmax. Why?
- [ ] [core] Softmax vs sigmoid: when each, and why
- [ ] [likely] Residual connections and layer norm inside a block
- [ ] [likely] The feed-forward block: what it does
- [ ] [likely] Which block takes the most compute: attention vs feed-forward? (and how it changes with sequence length)
- [ ] [likely] Attention complexity is O(n²) in sequence length: what that costs and what mitigates it
- [ ] [likely] Causal (masked) attention: what the mask does and why decoders need it
- [ ] [core] Encoder-only (BERT) vs decoder-only (GPT) vs encoder-decoder (T5): what each is good for
- [ ] [likely] Why decoder-only won for the LLM era
- [ ] [deep] Grouped-query / multi-query attention: what they change and why (inference memory)
- [ ] [deep] FlashAttention: what problem it solves (memory I/O, not the math) [gap]
- [ ] [deep] Pre-norm vs post-norm [gap]

### After / beyond the standard transformer
- [ ] [likely] What comes after the transformer architecture? Be able to name the main directions and say honestly how far each has gotten
- [ ] [likely] Mixture of Experts (MoE): what it is, why it saves compute per token, and the tradeoffs (memory, routing, load balancing) [gap]
- [ ] [deep] State-space models / linear-attention alternatives at a conceptual level [gap]
- [ ] [deep] Total parameters vs active parameters

### Inference mechanics
- [ ] [core] KV cache: what it stores and why it helps
- [ ] [core] Is KV cache used in training or in inference? Why?
- [ ] [likely] Prefill vs decode phase; why the first token is slower than the rest
- [ ] [likely] How KV cache memory grows with context length and batch size
- [ ] [likely] Sampling: temperature, top-k, top-p; what each changes; when you'd use temperature 0
- [ ] [likely] Why the same prompt at temperature 0 can still vary a bit across runs
- [ ] [likely] Frameworks for inference (e.g. vLLM, llama.cpp, TGI, TensorRT-LLM) and what each is for [gap]
- [ ] [deep] Continuous batching and paged attention: what problem they solve [gap]
- [ ] [deep] Speculative decoding in plain words [gap]
- [ ] [deep] Latency metrics: time to first token, tokens per second, throughput vs latency tradeoff

---

## 6. LLM fundamentals: tokens, embeddings, context
*Taught in: [Phase 4 - LLMs & Applied AI Engineering](../phase-4-llm-engineering/) (topic 1 and 2).*

- [ ] [core] What a token is; Byte-Pair Encoding in plain words
- [ ] [core] Why token count ≠ word count; how that affects cost and limits (and non-English text)
- [ ] [core] What an embedding is; why similar meanings land near each other
- [ ] [core] Embedding model vs generative model: how they differ
- [ ] [core] Context window: input + output share the budget
- [ ] [likely] What happens when you exceed the context window; truncation strategies
- [ ] [likely] "Lost in the middle": why a longer context isn't always better
- [ ] [likely] Why LLMs hallucinate, and the ways to reduce it
- [ ] [likely] Pretraining vs instruction tuning vs preference tuning: what each stage adds
- [ ] [deep] Scaling laws at a conceptual level: what "more data / params / compute" buys [gap]
- [ ] [deep] Prompt caching: what's cached, why it cuts cost and latency

---

## 7. Fine-tuning, alignment & quantization
*Taught in: [Phase 4 - LLMs & Applied AI Engineering](../phase-4-llm-engineering/) (topic 3), plus the LoRA paper from the reading list.*

- [ ] [core] Fine-tuning vs prompting vs RAG: how you choose for a given problem
- [ ] [core] Fine-tuning techniques: full vs parameter-efficient
- [ ] [core] LoRA: what's frozen, what's trained, what low-rank means, what rank r controls
- [ ] [core] QLoRA: how it differs from LoRA and what it makes possible
- [ ] [core] What does "3B" or "13B" parameters mean? Estimate the memory to load it at fp16, int8, int4
- [ ] [core] Quantization techniques: what it trades away and what it saves; post-training vs quantization-aware; name a few formats/methods [gap]
- [ ] [likely] Supervised fine-tuning (SFT): what the data looks like (instruction/response pairs)
- [ ] [likely] Catastrophic forgetting and how PEFT mitigates it
- [ ] [likely] How you'd build a fine-tuning dataset, and how much data is enough
- [ ] [likely] Overfitting in fine-tuning: signs and fixes
- [ ] [likely] How context windows work: input + output share the budget (also covered above; be able to say it both ways)
- [ ] [deep] RLHF in outline: reward model, policy optimization [gap]
- [ ] [deep] DPO: how it differs from RLHF [gap]
- [ ] [deep] GRPO and GSPO (advanced): what problem each addresses and how they relate to PPO; say honestly what you do and don't know [gap]
- [ ] [deep] Distillation: what it is and why it's used [gap]
- [ ] [deep] Merging adapters / serving many LoRA adapters on one base model [gap]

---

## 8. RAG
*Taught in: [Phase 4 - LLMs & Applied AI Engineering](../phase-4-llm-engineering/) (topics 4 and 5, plus the capstone).*

### Concepts & components
- [ ] [core] What RAG is, and what problem it solves vs fine-tuning
- [ ] [core] Components of a RAG system: ingest → chunk → embed → store → retrieve → (rerank) → generate
- [ ] [core] How similarity search works underneath; why vector DBs aren't "just databases"
- [ ] [core] Cosine similarity vs dot product vs Euclidean distance: when each, and when they're equivalent
- [ ] [likely] Vector DB options (Chroma, Pinecone, Weaviate, pgvector) and how you'd pick one
- [ ] [likely] Approximate nearest neighbor search and why exact search doesn't scale (HNSW, IVF at a conceptual level) [gap]
- [ ] [likely] Metadata filtering and why it matters (multi-tenant, access control, date ranges)

### Chunking
- [ ] [core] Chunking strategies: semantic, recursive, paragraph, token-based; overlap
- [ ] [core] On what basis do you choose a chunking strategy? (document type, query type, embedding model limits)
- [ ] [likely] Chunk size tradeoff: too small vs too big
- [ ] [likely] Handling tables, code, PDFs, scanned documents
- [ ] [deep] Parent-child / small-to-big retrieval; adding context to chunks

### Retrieval quality
- [ ] [core] Hybrid vs dense search: what each finds and misses
- [ ] [core] Cosine similarity (dense, vectors) vs BM25 (sparse, keyword scoring): they're different kinds of things; say how
- [ ] [core] What reranking does internally (bi-encoder vs cross-encoder)
- [ ] [core] Scenario: the relevant result shows up at position 4, 5, or 6. How do you fix it?
- [ ] [likely] Query rewriting, multi-query, HyDE: what each does
- [ ] [likely] Top-K choice: what happens if K is too small or too large
- [ ] [likely] Retrieval is fine but the answer is still wrong: how do you tell which half is failing?
- [ ] [likely] Retrieved chunks are irrelevant: a debugging checklist (chunking, embedding model, query, filters)
- [ ] [deep] Reciprocal rank fusion for combining dense and sparse results

### Production scenarios
- [ ] [core] Scenario: output was good for 1-2 months, then quality degrades. What's the issue and how do you fix it? (data drift, stale index, new document types, embedding/model changes, no monitoring)
- [ ] [likely] How do you keep the index fresh: incremental updates, deletes, re-embedding after a model change
- [ ] [likely] Citations: how do you make answers traceable to source chunks
- [ ] [likely] Preventing the model from answering when retrieval found nothing
- [ ] [deep] Multi-tenant RAG: isolating one customer's documents from another's
- [ ] [deep] Latency and cost budget for a RAG request; where you'd cut

### Evaluation (see also section 9)
- [ ] [core] How do you measure retrieval quality vs generation quality separately?
- [ ] [likely] Relevance, faithfulness, answer correctness against a labeled set

---

## 9. Evaluation
*Taught in: [Phase 4 - LLMs & Applied AI Engineering](../phase-4-llm-engineering/) (topic 5) and [Phase 5 - Agent Engineering & Production](../phase-5-agents/) (harnesses).*

- [ ] [core] How do you know an LLM app actually works, not by vibes?
- [ ] [core] Build a small labeled eval set: what goes in it and how many examples to start
- [ ] [core] Retrieval metrics: precision@k, recall@k, MRR, hit rate; what each tells you
- [ ] [likely] Generation metrics: faithfulness/groundedness, answer relevance, correctness
- [ ] [likely] LLM-as-judge: strengths, biases, and how you'd validate the judge
- [ ] [likely] Offline eval vs online eval (user feedback, A/B tests)
- [ ] [likely] Regression testing prompts; a CI evaluation gate
- [ ] [likely] Tools you can name and what they're for: RAGAS, Arize Phoenix, LangSmith, Braintrust
- [ ] [deep] Your own eval story: "precision went from X to Y after changing chunking"
- [ ] [deep] Non-determinism: how you evaluate outputs that vary run to run

---

## 10. Prompting & structured output
*Taught in: [Phase 4 - LLMs & Applied AI Engineering](../phase-4-llm-engineering/) (topic 6).*

- [ ] [core] Zero-shot vs few-shot vs chain-of-thought: when each helps
- [ ] [core] System vs user vs assistant roles; what goes where
- [ ] [core] Forcing structured/JSON output: prompt-only vs schema/constrained decoding vs function calling
- [ ] [likely] What to do when the model returns invalid JSON (validation, retry, repair)
- [ ] [likely] Pydantic schemas as the contract for LLM output
- [ ] [likely] Prompt versioning and testing prompts like code
- [ ] [likely] Reducing hallucination through prompting (grounding, "say you don't know", citations)
- [ ] [deep] Long prompts: ordering, delimiters, where to put instructions vs context

---

## 11. LangChain / LangGraph
*Taught in: [Phase 4 - LLMs & Applied AI Engineering](../phase-4-llm-engineering/) (topic 6, light touch) and [Phase 5 - Agent Engineering & Production](../phase-5-agents/).*

- [ ] [core] LangChain vs LangGraph: what each is for and when you'd choose which
- [ ] [core] Creating an agent in LangChain vs LangGraph
- [ ] [core] How do you create a graph? Which class?
- [ ] [core] Flow of building a graph: state, nodes, edges (including conditional edges), compile, invoke
- [ ] [core] What the graph "state" is and how nodes update it (reducers)
- [ ] [core] What is a checkpointer for?
- [ ] [core] What happens if you delete / don't use the checkpointer? (no persistence, no resume, no thread memory, no human-in-the-loop)
- [ ] [likely] Thread IDs and how conversations are separated
- [ ] [likely] Memory: short-term (within a thread), long-term (across threads), episodic; where each is stored
- [ ] [likely] Human-in-the-loop (HITL): which class / mechanism? (interrupts and resume)
- [ ] [likely] Streaming outputs from a graph
- [ ] [likely] Error handling, retries, and timeouts inside nodes
- [ ] [likely] Debugging and tracing a graph run (LangSmith)
- [ ] [deep] Scenario: JSON-based dynamic graph creation (build a graph from a config at runtime; validation, safety limits)
- [ ] [deep] Subgraphs and multi-agent patterns (supervisor, handoff, parallel branches)
- [ ] [deep] When you would *not* use a framework at all

---

## 12. Agents, tools, MCP & A2A
*Taught in: [Phase 4 - LLMs & Applied AI Engineering](../phase-4-llm-engineering/) (topic 6) and [Phase 5 - Agent Engineering & Production](../phase-5-agents/).*

- [ ] [core] What an agent is vs a plain LLM call vs a fixed workflow
- [ ] [core] The basic agent loop: reason → choose tool → run → observe → repeat → stop
- [ ] [core] How tool/function calling works under the hood (the model emits a structured request; your code runs it)
- [ ] [core] MCP vs a plain tool: what MCP standardizes and what it adds
- [ ] [core] Agent chain A → B → C → D (remote): the A2A protocol, and how it differs from MCP
- [ ] [likely] Planning patterns: ReAct, plan-and-execute, reflection
- [ ] [likely] Why agents fail: loops, wrong tool choice, bad arguments, compounding errors
- [ ] [likely] Guardrails on tools: allowlists, argument validation, confirmation for risky actions
- [ ] [likely] How you'd limit cost and runaway loops (max steps, budgets, timeouts)
- [ ] [likely] Tool design: good names, descriptions, narrow scope
- [ ] [deep] Multi-agent systems: when more agents help and when they only add cost
- [ ] [deep] Agent memory design: what to store, summarize, forget
- [ ] [deep] Evaluating an agent end-to-end vs step by step; replay and trace-based debugging

---

## 13. Safety & security for LLM apps
*Taught in: [Phase 5 - Agent Engineering & Production](../phase-5-agents/) (production hardening).*

- [ ] [core] Prompt injection: direct vs indirect; why it's hard to fully prevent
- [ ] [likely] Defenses: least privilege for tools, separating instructions from data, output validation, confirmations
- [ ] [likely] PII and sensitive data: what you send to a third-party API, and redaction
- [ ] [likely] Data leakage across users in RAG or memory
- [ ] [likely] Jailbreaks and content moderation layers
- [ ] [deep] Excessive agency: giving an agent tools it doesn't need
- [ ] [deep] Secrets and API keys: handling and rotation

---

## 14. Production LLM engineering
*Taught in: [Phase 5 - Agent Engineering & Production](../phase-5-agents/).*

- [ ] [core] Cost optimization: model routing, smaller models for easy tasks, caching, shorter prompts
- [ ] [core] Latency optimization: streaming, parallel calls, caching, smaller context
- [ ] [likely] Reliability: retries with backoff, timeouts, rate-limit handling, fallback models
- [ ] [likely] Observability: logs, traces, token/cost tracking, quality monitoring
- [ ] [likely] Semantic caching vs exact caching vs provider prompt caching
- [ ] [likely] Queues and background jobs for long-running LLM work
- [ ] [likely] Versioning prompts, models, and indexes; safe rollout and rollback
- [ ] [deep] Detecting quality regressions after a model provider silently updates a model
- [ ] [deep] Capacity planning: tokens per request × requests per second × cost

---

## 15. System design scenarios
*Practice after Phase 4 and 5. Talk through requirements, architecture, data flow, failure modes, evaluation, cost.*

- [ ] [core] Design a chatbot over a company's internal documents (RAG end to end)
- [ ] [core] Design a customer-support assistant that can look up orders and issue refunds (tools + guardrails + HITL)
- [ ] [likely] Design a document-processing pipeline that extracts structured data from thousands of PDFs
- [ ] [likely] Design a research/analyst agent that searches, summarizes, and cites
- [ ] [likely] Design a code-review or code-assist agent
- [ ] [likely] Design the streaming chat UI and backend (SSE/WebSocket, partial rendering, cancellation, retries)
- [ ] [deep] Design an LLM gateway: routing, caching, rate limiting, cost tracking across teams
- [ ] [deep] Design an eval and monitoring system for an LLM product
- [ ] [deep] Scale a RAG system from 10K to 100M documents

---

## 16. Frontend × AI (your edge)
*Where your existing skills merge in. Have a confident answer for each.*

- [ ] [likely] How you stream LLM tokens to a React UI (SSE vs WebSocket vs fetch streaming) and handle cancellation
- [ ] [likely] Rendering partial markdown/JSON safely while it streams
- [ ] [likely] Showing tool calls, citations, and uncertainty in the UI
- [ ] [likely] Optimistic UI and error states when the model is slow or fails
- [ ] [likely] Where to keep API keys (never in the browser) and how your Next.js route handlers proxy calls
- [ ] [deep] Collecting user feedback (thumbs up/down) and feeding it back into evals

---

## 17. Personal projects
*Fill in as you build. Capstones from Phase 4 and 5 go here.*

- [ ] [core] One-minute pitch per project: problem, architecture, hardest bug, what you'd change
- [ ] [core] Eval story: the numbers before and after a change
- [ ] [core] Why you made each major choice (chunking, vector DB, model, framework)
- [ ] [likely] What failed, and what you learned from it
- [ ] [likely] How you'd scale it 100× and what breaks first
- [ ] [likely] Cost per request and how you'd cut it
- [ ] [likely] Walk through the repo live: structure, key files, how to run it

---

## 18. Certifications
*Only if completed.*

- [ ] [core] AWS Certified Developer – Associate: what it covers and one thing you applied from it

---

## 19. Cloud (AWS, Azure)
*Resource names and what each is used for.*

- [ ] [core] AWS: compute (EC2, Lambda, ECS/EKS), storage (S3), DB (RDS, DynamoDB), queues/events (SQS, SNS, EventBridge), IAM, networking (VPC, ALB, API Gateway), secrets (Secrets Manager / Parameter Store), logs (CloudWatch)
- [ ] [core] Azure: the same categories mapped to AWS equivalents (VMs, Functions, AKS, Blob, Cosmos/SQL, Service Bus, Entra ID/RBAC, VNet, Key Vault, Monitor)
- [ ] [core] Which services did you actually use in your projects, and why
- [ ] [likely] Managed LLM services on each cloud (e.g. Bedrock on AWS, Azure OpenAI): when you'd use one over calling a provider directly [gap]
- [ ] [likely] How you'd secure a deployed LLM app (IAM roles, secrets, network, least privilege)
- [ ] [likely] Cost control: budgets and alerts, avoiding idle resources

---

## 20. Deployment
*Only what you've actually done.*

- [ ] [core] Docker: image vs container, Dockerfile for a FastAPI app, layer caching, keeping images small
- [ ] [core] CI/CD: GitHub Actions workflow (test → build → deploy)
- [ ] [core] Hosting options: AKS, Lambda, App Service, ACS. When each fits
- [ ] [likely] Environment variables and secrets in deployment
- [ ] [likely] Health checks, logging, and rollbacks
- [ ] [likely] Cold starts on serverless and why they matter for LLM apps
- [ ] [likely] Where the vector DB and any model server live in your deployment
- [ ] [deep] Blue/green or canary releases for prompt or model changes

---

## 21. Behavioral & positioning
*Your story matters as much as the technical answers.*

- [ ] [core] "Why are you moving from frontend into AI engineering?" (a 60-second answer)
- [ ] [core] What do you bring that a pure ML candidate doesn't? (UX, product shipping, production engineering, API/cloud experience)
- [ ] [likely] Where is your knowledge still shallow, and how are you closing the gap? (honest answer, with a plan)
- [ ] [likely] A time you debugged something hard in production
- [ ] [likely] How you keep up with a fast-moving field without chasing every new thing
- [ ] [likely] How you decide whether a problem needs an LLM at all
- [ ] [likely] How you explain a technical tradeoff to a non-technical stakeholder
