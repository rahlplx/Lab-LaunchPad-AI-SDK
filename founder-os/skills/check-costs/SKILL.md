---
name: check-costs
description: Review the project's actually-wired integrations (.mcp.json) for potential billing surprises and explain them in plain language. Use before /ship-checklist's first real deploy, whenever a new service is integrated, or any time the founder asks "will this cost me money."
---

# Check Costs

A non-technical founder often doesn't realize API calls, database
queries, or hosting bandwidth have costs until a surprise bill arrives.
This skill exists to surface that risk before it becomes a bill, using
what's actually configured, not a generic warning.

## What to do

1. **Read `.mcp.json` to see what's actually wired** — don't warn about
   services that aren't connected. Cross-reference each configured
   server against `references/mcp-servers.md` for its known cost shape
   (e.g. Stripe moves real money on live-mode actions, PostHog can bill
   certain tool calls as "AI spend," cloud-resource creation is
   inherently metered).

2. **Name the specific trigger for each real cost risk**, not a vague
   "this could cost money" — e.g. "switching Stripe out of test mode
   means every charge from here is real" or "creating a new Supabase
   project on a paid tier bills monthly regardless of usage."

3. **Cross-check against `policy.json`'s `cost_sensitive` category
   rules** (`cost-cloud-resource-create`, `cost-stripe-live-mode-toggle`)
   — these already pause for confirmation on the riskiest actions; this
   skill's job is to explain *why* before the founder hits that prompt,
   not to duplicate the gate itself.

4. **Give one plain-language number where possible** — "this tier is
   $X/month regardless of traffic" beats "this has a cost." If the exact
   number isn't knowable from what's configured, say so explicitly
   rather than guessing.

5. **End with a clear go/no-go-shaped summary**: what's currently free or
   effectively free, what has a real ongoing cost already committed, and
   what would newly start costing money if the founder proceeds with
   what they're about to do.

## Anti-patterns to avoid

- Generic disclaimers ("cloud services can cost money") instead of
  naming the specific service and trigger.
- Scaring the founder off free-tier usage that's genuinely fine at their
  current scale.
- Guessing a specific dollar amount when the real pricing isn't actually
  knowable from what's configured — say "check the current pricing page"
  instead of inventing a number.
