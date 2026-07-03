---
name: read-analytics
description: Interpret PostHog/Plausible (or equivalent) analytics data in plain language and turn it into one clear next action. Use after /plan-launch, or any time the founder asks "how's it doing" or pastes in numbers/a dashboard screenshot.
---

# Read Analytics

A non-technical founder can look at a dashboard full of charts and not
know what to do next. This skill's only job is to turn numbers into one
plain-language sentence and one next action — not a data-science
lecture.

## What to do

1. **Get the real numbers**, not a guess. Use the `posthog` MCP server
   directly if configured (check `.mcp.json`), or ask the founder to
   paste the specific numbers/screenshot if it isn't. Don't estimate or
   assume metrics that weren't actually provided.

2. **Anchor to the one goal that matters**, the launch-week goal set in
   `/plan-launch` (or ask for it if this is the first time). Compare
   against that goal specifically, not a generic "engagement" summary.

3. **Say it in one plain sentence first**: "X people did the core action
   out of Y who tried, which is [above/below/roughly at] your goal of
   Z." Lead with that sentence before any supporting detail.

4. **Name the single biggest drop-off**, if there is a funnel (signed up
   → tried the core feature → came back). Founders need to know *where*
   people are leaving, not just that some did.

5. **End with exactly one next action**, not a list of five possible
   experiments — e.g. "the biggest drop-off is between signup and first
   use, so let's look at what that first-use flow actually asks people
   to do." Hand off to `/debug-seb` or `/refactor-safely` if the action
   is product-side, or back to `/plan-launch` if the action is
   distribution-side.

## Anti-patterns to avoid

- Drowning the founder in every available metric instead of the one that
  maps to their stated goal.
- Suggesting a redesign or pivot off of day-one numbers — most signal
  needs at least a few days/dozens of users before it's real signal, not
  noise.
- Presenting analytics jargon (cohorts, retention curves, funnels) without
  translating it into what actually happened to actual people.
