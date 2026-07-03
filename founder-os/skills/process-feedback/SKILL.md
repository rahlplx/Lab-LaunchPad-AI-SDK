---
name: process-feedback
description: Turn raw user feedback (support messages, reviews, DMs, calls) into a prioritized, actionable backlog instead of a vague pile of complaints. Use whenever the founder has feedback to process, especially right after /plan-launch's launch window.
---

# Process Feedback

Feedback arrives as scattered, emotional, inconsistent raw text. A
founder who can't read code also often can't turn "this is confusing"
into a specific fix. This skill's job is that translation.

## What to do

1. **Collect the raw feedback as-is first** — don't paraphrase or
   summarize before recording it. Ask the founder to paste messages,
   reviews, or a rough transcript of what people said, verbatim.

2. **Sort each item into exactly one bucket**: a specific bug (something
   broken), a specific confusion point (something unclear, but working
   as built), a feature request (something that doesn't exist yet), or
   noise (too vague to act on — needs a follow-up question, not a fix).

3. **Convert bugs and confusion points into backlog items with the
   WHEN/THEN shape** `/founding-prompt`'s `PRD.md` already uses — e.g.
   "WHEN a user clicks Save with an empty field THEN nothing happens and
   there's no error message" — so they're immediately actionable by
   `/build-feature` or `/fix-bug`, not still vague.

4. **Weigh feature requests against the existing non-goals list** in
   `PRD.md` before adding them anywhere — a request that fits a
   deliberate non-goal isn't automatically scope creep to reject, but it
   is a decision the founder should make explicitly, not one this skill
   makes for them.

5. **Report back a short prioritized list**, ranked by how many people
   hit the same issue, not by which was most recently said or most
   loudly complained about.

## Anti-patterns to avoid

- Turning every complaint into an immediate to-do without checking if
  multiple people hit the same thing — one person's opinion isn't
  automatically a priority.
- Silently expanding scope by treating every feature request as accepted
  — the founder decides, this skill organizes.
- Losing the original wording — "confusing" said three different ways by
  three users is a real, specific signal; don't compress it away too
  early.
