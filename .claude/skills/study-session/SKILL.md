---
name: study-session
description: Start or resume today's roughly 1-hour AI-engineering study session in the study tracker. Use when the user says "start today's session", "continue", "next lesson" or "what's next".
---

# Study session

Run one study session for the current phase, following the teaching rules in the root `CLAUDE.md`.

## Steps

1. Read `study-tracker/PROGRESS.md`. The current phase is the one marked 🟦; if none, it is the first ⬜ phase and you should mark it 🟦 with today's date after confirming with the user. Read the last 3 rows of the daily log to see where he stopped.
2. Read that phase's `README.md`, `CHECKPOINT.md` and the matching section of `study-tracker/docs/curated-resources.md`. Look in `notes/` to see which concepts already have notes.
3. Pick the **next un-covered concept** from the phase topic list. Do not skip ahead or pull from another phase. If he asks about something outside the phase, say it is a detour and offer to park it.
4. Say in one line what today's 1-hour plan is (2 or 3 chunks of 20-30 minutes) and which curated resource, if any, goes with it.
5. Teach **one chunk at a time**: intuition, then math (numeric example first, every step shown), then code. Define jargon on first use. Link the concept to tools he already uses (tokens, context windows, sampling, RAG, agents).
6. End each concept with 2-3 check questions. **Stop and wait for his answers.** Mark them, correct gaps, and only then continue. For math concepts also give 2-3 practice problems.
7. When the session ends, or he says he is done, run the `log-session` skill.

## Rules

- No new resources beyond `curated-resources.md`.
- Never answer your own check questions or move on without his answers.
- Keep it to about an hour; stop at a clean boundary and say where tomorrow starts.
