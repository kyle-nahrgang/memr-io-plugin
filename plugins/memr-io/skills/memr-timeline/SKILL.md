---
name: memr-timeline
description: Use when recording or asking about events in someone's life with memr.io — moves, jobs, schools, trips, relationships, milestones — or the people, places and organizations in them. Triggers include "put it on my timeline", "when did I…", "add my trip to…", "I started a new job", "remember my friend…".
---

# The memr.io timeline

Life events in memr.io are records with dates, sources and links, not chat summaries. Get them right the first
time: every other assistant the person uses will read them.

## Before you add

1. **Search first**, with the words the event would use, and try a second phrasing. Search matches words, not
   meaning. If the event exists, `update` it; if something close exists, ask.
2. **Find or create the people, places and organizations** it involves (`search` kind=person/place/org), then
   pass their ids (`person_ids`, `place_ids`, `org_ids`) or use `link` afterwards.

## Writing an event

| Field | How |
|---|---|
| `title` | Short and specific: "Moved to Denver", "Started at Acme as a designer". |
| `summary` | One diary line: past tense, no subject, no "I", no name. "Moved into a two-bedroom near the park." |
| `lane` | `home`, `career`, `education`, `relationship`, `travel`, `life`, or `other`. |
| `start` / `end` | `YYYY`, `YYYY-MM` or `YYYY-MM-DD`, only as precise as the evidence. Never guess a day. A span that hasn't ended is `ongoing`. |
| `importance` | 9-10 defines a life (a marriage, a child), 7-8 a milestone (a move, a new job), 5-6 notable (a big trip), 3-4 detail, 1-2 trivia. |
| `source` | Required. `from-<name>` when the person told you, `email: <account>, <date>, <subject>`, `file: <name>`, or a public record. |
| `confidence` | `confirmed` (they said so, or a document shows it), `inferred` (a reasonable reading), or `unknown` (a placeholder: say so). |
| `detail` | Clear prose in your own words: what happened, why, guesses and how you know. Not a quote of the person. |

A trip or a job can hold child events (`parent_id`): a promotion under a job, a stop under a trip.

## Gaps are fine

- A rough date is better than none. memr.io lists imprecise dates as "dates to find"; `search` `needs_date` shows
  them.
- If an event is too thin to be useful, `update` it with `needs_detail` set to the question to ask. Clear it
  (empty string) once the detail is in. `search` `needs_detail` lists them.
- Don't fill a gap with a guess presented as fact.

## Private by default

- Relationships, health and money: one summary line, no copied detail, and mark it `sensitive`.
- Never store email addresses, account numbers, passwords or street addresses. Places are city or neighborhood
  level.

## Answering questions

"When did I…?" or "what happened in 2019?": `search` with a query, or with `from`/`to` (and `lane`) for a range,
then `get` the events that matter. Say how sure the record is when it isn't `confirmed`.
