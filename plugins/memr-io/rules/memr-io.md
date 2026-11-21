# Working with memr.io

memr.io (said "mem'ry'oh") holds this person's to-dos, notes, memory notes and a life timeline. Any assistant they connect sees the same entries, so treat it as shared, lasting state.

- **Search before you create.** Before adding a to-do, page, person or event, search for it (try a couple of
  phrasings). If a match exists, update it. If something is close but you are not sure it is the same thing, ask
  the person rather than guessing.
- **Save what lasts, skip what doesn't.** To-dos they commit to, decisions, lasting facts and preferences, and
  real milestones. Not passing moods, chores they did not ask you to track, or things you only looked up.
- **Keep to-dos small and actionable.** A short, verb-first name; due dates and owners only when the person gives
  them; blocked_by only for real dependencies.
- **Finishing a to-do means setting its status.** When work is finished, or the person says it is, `update` it with
  `status` `done`, then check that the status took. Writing "Done" into the detail leaves it open on their list,
  and they end up asking again.
- **Tasks on an event, and expired ones.** A to-do can sit inside an event (`parent_id` = the event) and is due when the
  event is; for an event that spans days, ask which day. Once the event has passed, a task still open reads as
  `expired`. Never delete or close those on your own: call `whats_next`, show them by event, and ask what to do
  with each (done, move the date, archive, delete). Use `plan_event` when they want help planning an event.
- **Tag quick wins.** A to-do that needs little effort or thought gets the tag `low-hanging-fruit`, so it is easy
  to find a short list of things to knock out.
- **Edit, don't rewrite.** Append to running notes; change only the fields that changed. Every write has a change
  number, so fix a mistake with `revert` instead of piling on corrections.
- **Be honest about certainty.** Give events a source and keep dates as precise as the evidence, no more.
- **Link, don't repeat.** Write `[[Title]]` to point at another entry instead of copying its content.
- **Search by the words the entry would use.** Search matches words, not meaning; try a second phrasing before
  deciding something isn't there.
- **Keep private things private.** No passwords, account numbers or street addresses; health, money and
  relationships stay one line and summary-level.
- **Say what you saved.** After writing, tell the person in a line what changed (counts or titles, not a dump).
