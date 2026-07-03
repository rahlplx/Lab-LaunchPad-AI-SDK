---
name: setup-monitoring
description: Guide setup of the 3 monitors every founder needs (uptime, errors, usage) using the Sentry/PostHog MCP servers already wired, and explain what the data actually means once it's flowing. Use once /ship-checklist has gone Green for a first real deploy, or whenever the founder asks "how would I know if something breaks."
---

# Setup Monitoring

A founder who can't read code has no way to notice a silent failure
except a user complaining — often much later than the failure itself.
This skill closes that loop using integrations already wired, not new
ones.

## What to do

1. **Confirm what's actually connected first.** Check `.mcp.json` for
   `sentry` (errors) and `posthog` (usage) — this skill wires up
   monitoring using what's already configured, it doesn't introduce new
   services. If a needed server isn't set up yet, hand off to
   `/integrate-service` first.

2. **Set up the 3 monitors, explained in plain language as you go:**
   - **Uptime** — is the product reachable at all right now? (Hosting
     platform's own status page/alerts, e.g. Vercel's.)
   - **Errors** — is something actually breaking for users? (Sentry:
     confirm error reporting is live, and that a deliberate test error
     actually shows up there before trusting it.)
   - **Usage** — are people actually using it, and how? (PostHog: confirm
     at least the core action from `PRD.md`'s behavior rules is being
     tracked as an event.)

3. **Verify each monitor actually fires**, don't just configure and
   assume. Trigger one real test error and confirm it appears in Sentry;
   confirm one real usage event appears in PostHog. Evidence over
   say-so, same as everywhere else in this plugin.

4. **Explain what a normal baseline looks like** once data is flowing —
   so the founder has something to compare an actual problem against
   later, not just a blank dashboard they don't know how to read.

5. **Say what to do when each monitor fires**, concretely: uptime down →
   check the hosting platform's status first; a new error spike in
   Sentry → hand off to `/debug-seb`; usage cratering → hand off to
   `/read-analytics` to figure out where people are dropping off.

## Anti-patterns to avoid

- Setting up a monitor and never confirming it actually fires on a real
  test signal.
- Recommending new monitoring tools/services instead of using what's
  already wired via `.mcp.json`.
- Drowning the founder in dashboard configuration options instead of the
  3 monitors that actually matter at this stage.
