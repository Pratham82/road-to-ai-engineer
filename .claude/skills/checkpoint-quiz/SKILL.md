---
name: checkpoint-quiz
description: Quiz the user against the current phase's CHECKPOINT.md before he advances, log results, and update phase status. Use when the user says "checkpoint", "am I ready for the next phase" or "quiz me on the phase".
---

# Checkpoint quiz

Gate between phases. He advances only when every checkpoint item is passed.

## Steps

1. Read the current phase's `CHECKPOINT.md` and its `notes/` and `project/` folders. Read `study-tracker/PROGRESS.md` for the phase status.
2. Go through the checkpoint items **one at a time**. For each: ask the question in your own words (a concrete numeric or code scenario, not a definition lookup), wait for his answer, then judge it honestly: pass, or retry with the specific gap named.
3. For items that require a project (for example an EDA in Pandas), check that the work exists in `project/` and review it rather than asking him to describe it.
4. After each item, add a row to the **Quiz log** table in `CHECKPOINT.md`: date, item, short answer summary, result (pass / retry).
5. Tick an item's box only after a pass. A retry stays unticked; offer a short re-teach and re-quiz it next session.
6. When **every** box is ticked, set the phase to ✅ in `PROGRESS.md` with the date, and tell him the next phase's starting point. Do not start the next phase in the same quiz. If any item is shaky, recommend extra time here instead of advancing.

## Rules

- Be strict. A vague answer is a retry. Never tick on his behalf.
- Questions come from the checkpoint items only; no new topics.
