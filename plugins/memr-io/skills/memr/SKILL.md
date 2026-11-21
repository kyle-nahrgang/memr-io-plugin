---
name: memr
description: Use for anything involving memr.io (said "mem'ry'oh") — adding, finding or finishing to-dos, checking what is ready or blocked, saving a note or memory, recording a life event, or reviewing recent changes. Triggers include "add a to-do", "what's on my list", "what can I start", "remember that…", "put it on my timeline", "memr".
---

# memr.io

memr.io is the person's shared store of to-dos, pages (projects, topics, goals, notes), memory notes and
timeline events. It is reached through the `memr-io` MCP tools: `whoami`, `search`, `get`, `add`, `update`,
`link`, `revert`, `recent_changes`, `start_project` and `start_timeline`. Say the name as "mem'ry'oh".

Related skills: **memr-setup** (new accounts and guided setup), **memr-timeline** (life events, people, places),
**memr-review** (what changed, undo, weekly review, tidying).

Follow the person's own rules (CLAUDE.md, AGENTS.md) where they differ from the habits below.

## First contact

Call `whoami` once per session if you have not yet. If it says `no_plan` or `first_run`, use the **memr-setup**
skill.

## Quick recipes

| They say | Do |
|---|---|
| "add a to-do: X" | `search` for X (kind=todo, a couple of phrasings) → if it exists, say so or `update` it; if close, ask; else `add` kind=todo |
| "what's on my list?" | `search` kind=todo (open by default); group by project if there are many |
| "what can I start?" / "what's blocked?" | `search` kind=todo `ready=true` / `blocked=true` |
| "what's next?" / "what should I do?" | `whats_next`: overdue, due soon, ready now, events coming up; then go through `needs_cleanup` (expired tasks) and ask what to do with each |
| "help me plan X" (a party, trip, move) | `plan_event`, and follow its script |
| "add a task to the X event" | `search` for the event, then `add` kind=todo with `parent_id` = the event (ask which day if the event spans days) |
| "quick wins" | `search` kind=todo `tag=low-hanging-fruit` |
| "done with X" | find it, then `update` `changes.status=done` |
| "X has to wait for Y" | `update` X with `changes.blocked_by=[Y's id]` |
| "remember that …" | `search` kind=memory first; `add` kind=memory, one fact per note |
| "add to my notes on X" | `update` with `append`, never rewrite the detail |
| "put it on my timeline" | use the **memr-timeline** skill |
| "what did you change?" / "undo that" | `recent_changes`, then `revert` the change number (see **memr-review**) |
| "this belongs under X" | `update` with `project` (or `parent_id`) set to the page's id |

## Habits

- **Search before you create; ask when it's close.** Duplicates are the most common mistake.
- **Tag quick wins** `low-hanging-fruit` when a to-do is small and needs little thought.
- **Link entries** by writing `[[Title]]` (or `[[Title|shown text]]`) in a summary or detail; `get` shows backlinks,
  and a write reports `unresolved_links` that match nothing yet.
- **Finish to-dos with `status` `done`**, not by writing "Done" in the detail.
- **Search matches words, not meaning.** Try the words the entry would use, and a second phrasing.
- **Groups:** tools work in the person's private space unless you pass a `group` id from `whoami`.
- **Respect the plan.** If a write is refused for a plan rule, say so plainly and carry on with what is allowed.
- **Report briefly.** One line on what was saved or changed.
