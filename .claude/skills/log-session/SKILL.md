---
name: log-session
description: Record a finished study session in the study tracker (daily log, concept note, progress status). Use when the user says "log this", "wrap up", "save today's session" or at the end of /study-session.
---

# Log session

Write down what actually happened in today's session. Record only what he really did and answered.

## Steps

1. Work out from the conversation: the phase, the concept(s) covered, whether he answered the check questions, and any shaky areas.
2. Append **one row** to the daily log table in `study-tracker/PROGRESS.md` (newest at the bottom): `| YYYY-MM-DD | Phase N | concept / chunk | yes / partly / no | short note |`. Replace the empty placeholder row if it is still there.
3. For each concept covered, create `study-tracker/phase-N-.../notes/YYYY-MM-DD-topic.md` containing: the intuition in his words, the worked numeric example, the key formula or code, his answers to the check questions, and anything he found shaky. Keep it short enough to re-read in 5 minutes. Do not overwrite an existing note; append a dated section instead.
4. Put any exercise or notebook he worked on in `exercises/`.
5. Update the phase status in `PROGRESS.md` only if it changed: ⬜ to 🟦 when a phase starts (fill `Started`). Do not mark ✅ here; only `checkpoint-quiz` does that.
6. Show a short summary of what was written and where. Commit on a branch with message `phase-N: <what he learned>` only if he asks.

## Rules

- Never invent answers or tick anything he did not do.
- Dates use the user's timezone (Asia/Calcutta).
