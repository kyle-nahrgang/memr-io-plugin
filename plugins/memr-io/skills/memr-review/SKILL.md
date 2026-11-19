---
name: memr-review
description: Use for a review or clean-up of someone's memr.io — "weekly review", "what changed", "what did you do", "undo that", "tidy up my list", "what's overdue", "find duplicates" — or after an assistant made changes the person wants to check.
---

# Reviewing memr.io

memr.io records every write as a numbered change. Use that to show the person what happened and to fix
mistakes cleanly.

## What changed, and undo

- `recent_changes` lists changes newest first: number, time, who (the person or which assistant), why, and the
  entries. Summarize it in a few lines; don't dump it.
- To undo, `revert` the change number. If it refuses because an entry changed again since, revert the later
  change first. A revert is itself a change and can be reverted.
- Fix a mistake with `revert`, not by layering corrections on top.

## Weekly review

Work through these, briefly, and ask before changing anything the person didn't ask you to change:

1. **Done:** to-dos finished this week (`search` kind=todo `status=done`), as a short list.
2. **Overdue and due soon:** open to-dos with a due date in the past or the next 7 days.
3. **Ready now:** `search` kind=todo `ready=true`. Suggest the top three.
4. **Blocked:** `search` kind=todo `blocked=true`, with what blocks each one. Ask whether any blocker is actually
   done.
5. **Quick wins:** `search` kind=todo `tag=low-hanging-fruit`.
6. **Stale:** open to-dos untouched for a long time. Ask: still wanted, done, or drop?

## Tidying

- **Duplicates:** search a couple of phrasings for the same thing. Show the pair and ask which to keep before
  merging; merge by updating the keeper and deleting (`update` `delete`) the other. Deleting hides an entry; it
  stays in history.
- **Finishing:** a to-do is finished only when its `status` is `done`. Writing "Done" in the detail leaves it open
  on their list.
- **Gaps on the timeline:** `search` `needs_date` and `needs_detail` list events waiting for a better date or more
  detail. Ask a few at a time, not all at once.

Close with one or two lines: what changed, what is next.
