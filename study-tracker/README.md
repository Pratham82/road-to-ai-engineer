# AI Engineer Study Tracker

My working folder for going from frontend engineer (React/Next.js/TS) to an AI engineer with real depth, not wrapper-level knowledge. It follows a fixed six-phase roadmap, in order, with no added resources.

## Phases

| # | Phase | Folder |
|---|---|---|
| 0 | Python for AI | [phase-0-python](phase-0-python/) |
| 1 | Math Foundations | [phase-1-math](phase-1-math/) |
| 2 | Classical ML | [phase-2-classical-ml](phase-2-classical-ml/) |
| 3 | Deep Learning & Transformers | [phase-3-deep-learning](phase-3-deep-learning/) |
| 4 | LLMs & Applied AI Engineering | [phase-4-llm-engineering](phase-4-llm-engineering/) |
| 5 | Agent Engineering & Production | [phase-5-agents](phase-5-agents/) |

Part of [road-to-ai-engineer](../README.md), which holds the wider reference material. Progress lives in [PROGRESS.md](PROGRESS.md). All resources are in [docs/curated-resources.md](docs/curated-resources.md).

## Layout of each phase folder

```
phase-N-.../
├── README.md       # the roadmap for this phase (source of truth)
├── CHECKPOINT.md   # exit criteria + quiz log; tick before advancing
├── notes/          # my own notes, one file per concept (YYYY-MM-DD-topic.md)
├── exercises/      # worked problems, practice sets, notebooks
└── project/        # the phase's project(s)
```

## Rules

1. Phases go in order. A phase is done only when every checkpoint box is ticked.
2. No new courses or resources beyond [docs/curated-resources.md](docs/curated-resources.md).
3. Every concept: intuition → math (numbers first, symbols second) → code → answer the check questions.
4. At least one public project + short write-up per phase from Phase 1 onward.

## Conventions

- Notes: `phase-N-.../notes/YYYY-MM-DD-topic.md`
- Notebooks: `exercises/` or `project/`, with outputs cleared before commit unless the output is the point
- Commits: `phase-N: <what you learned or built>`
- Python env: one per phase or one shared, your call; keep it out of git (see `.gitignore`)
