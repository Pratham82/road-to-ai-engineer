# How to use this tracker day to day

About an hour a day. Open Claude Code in the repo root (the root `CLAUDE.md` loads the tutor rules automatically), then follow the loop below.

## The daily loop

1. **Start:** run `/study-session`. Claude finds the current phase and where you stopped, then teaches the next concept one 20-30 minute chunk at a time (intuition, math with numbers first, code).
2. **Answer the check questions.** Claude waits for your answers after each concept. Do not skip them; a wrong answer is the point.
3. **Do the practice problems** for any math concept. Put working in `exercises/`.
4. **Wrap up:** run `/log-session`. Claude adds a row to the daily log in [PROGRESS.md](PROGRESS.md) and writes a note in `phase-N-.../notes/YYYY-MM-DD-topic.md`.
5. **End of phase:** run `/checkpoint-quiz`. Claude quizzes you against that phase's `CHECKPOINT.md`. Only when every box is ticked does the phase turn ✅.

## Skills

| Command | When | Writes to |
|---|---|---|
| `/study-session` | Start of every session | nothing (teaches); sets a phase to 🟦 on first start |
| `/log-session` | End of every session | `PROGRESS.md`, `notes/`, `exercises/` |
| `/checkpoint-quiz` | When a phase feels done | `CHECKPOINT.md` quiz log, `PROGRESS.md` status |

The skills live in `.claude/skills/`. Edit them if the routine should change.

## Where things go

| What | Where |
|---|---|
| What to study | `phase-N-*/README.md` |
| Books and courses | [docs/curated-resources.md](docs/curated-resources.md) |
| Your notes | `phase-N-*/notes/YYYY-MM-DD-topic.md` |
| Practice and notebooks | `phase-N-*/exercises/` |
| Phase project and write-up | `phase-N-*/project/` |
| Exit criteria and quiz log | `phase-N-*/CHECKPOINT.md` |
| Status and daily log | [PROGRESS.md](PROGRESS.md) |

## Ground rules

- Phases go in order; no starting the next one until the checkpoint is fully ticked.
- No new resources beyond the curated list. A tempting new topic is a detour; Claude will say so and bring you back.
- Weak at math? Say "slower" or "another example". Claude should always show worked steps with numbers first.
- Commit on a branch as `phase-N: <what you learned or built>` and open a PR.

## Quick prompts

- "Start today's session" or `/study-session`
- "Slower, show the numbers again"
- "Quiz me on what we did yesterday" (before starting new material)
- "Log this" or `/log-session`
- "Am I ready for the next phase?" or `/checkpoint-quiz`
