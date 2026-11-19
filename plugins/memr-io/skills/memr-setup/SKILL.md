---
name: memr-setup
description: Use when someone is new to memr.io or asks to get set up — "set me up with memr.io", "get started", "start a project", "set up my memory", "start a timeline" — or when memr.io's whoami reports first_run or no_plan.
---

# Setting up memr.io

## Check the account first

Call `whoami` once at the start of the session and act on what it reports:

| whoami says | Do |
|---|---|
| `no_plan` | There is no free plan, so nothing can be saved yet. Tell the person they can start the 14-day free trial of Personal at https://memr.io/billing, and add nothing until they have. |
| `first_run` | Nothing is saved yet. Offer to set up their first project (below). Don't start without a yes. |
| neither | They are set up. Skip this skill unless they asked for setup. |

## Run the interview, don't read it

`start_project` and `start_timeline` return an interview script. The script is for you, not the person:

- Follow it step by step, asking **one question at a time** in your own words.
- Never paste or read the script aloud, and don't mention that there is one.
- Keep to its time budget (about 10 minutes for a project, 5 for a timeline). If the person wants to stop early,
  save what you have and stop.

**Start a project** (`start_project`): when they say "set me up", "get started", or "start a project". The result is
one project page with a short list of to-dos, each with an owner and due date only if they gave one, and
`blocked_by` only for real dependencies. End by showing what they can start right now (`search` kind=todo
`ready=true`).

**Start memory and a timeline** (`start_timeline`): when they ask to set up memory or a timeline, or say yes when you
offer it at the end of a project setup. The result is a few lasting `memory` notes (preferences, facts they want
remembered) and the big events of their life so far. Use the **memr-timeline** skill's rules for the events.

## Show it travels

After setup, suggest the two-minute check from https://memr.io/start: open a new chat (or another assistant with
memr.io connected), ask "what can I start right now?", and see the same list.

## While setting up

- Search before you add, even in a new account: the person may have added something from another assistant.
- Don't ask for email addresses, account numbers, passwords or street addresses.
- If a write is refused for a plan rule, say so plainly and carry on with what is allowed.
- Finish with one or two lines on what was saved: counts and titles, not a dump.
